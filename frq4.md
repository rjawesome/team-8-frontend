## FRQ 4: Lightboard

# Default Lightboard

<button onclick="generateLightboard();">Generate Lightboard</button>
<div id="defaultLightboard"></div>

# Color Lightboard
<input id = "color">
<button onclick="generateColorLightboard();">Generate Lightboard</button>
<div id="colorLightboard"></div>


<script> 
    function generateLightboard() {
        var xhr = new XMLHttpRequest();
        xhr.open('GET', 'https://csa-backend.rohanj.dev/api/light1/getlights', true);
        xhr.onload = function () {
          if (xhr.status === 200) {
            // If the request was successful, create an HTML table with the response data
            var response = xhr.responseText;
            console.log(response);

            var response = JSON.parse(xhr.responseText);
            var result = document.getElementById("defaultLightboard");
            result.innerHTML = "";
            console.log(result);
            for (var i = 0; i < response.length; i++) {
                var lightData = response[i];
                console.log(lightData.light);
                var displayLight = document.createElement("div");
                displayLight.style.backgroundColor = 'rgb(' + [lightData.light.red,lightData.light.green,lightData.light.blue].join(',') + ')';
                displayLight.style.width = "100px";
                displayLight.style.height = "100px";
                
                displayLight.style.float = "left";
                if (lightData.column === 5) {
                    result.append(displayLight);
                    var placeholder = displayLight.cloneNode(true);
                    placeholder.style.float = "none";
                    result.append(placeholder);
                } else {
                    result.append(displayLight);
                }
                

                
            }


          } else {
            // If the request was unsuccessful, display an error message
            alert('Request failed. Returned status of ' + xhr.status);
          }
        };
        xhr.send();
    }

    function generateColorLightboard() {
        var colorChosen = document.getElementById("color").value;
        var xhr = new XMLHttpRequest();
        xhr.open('GET', 'https://csa-backend.rohanj.dev/api/light1/getlights/' + colorChosen, true);
        xhr.onload = function () {
          if (xhr.status === 200) {
            // If the request was successful, create an HTML table with the response data
            var response = xhr.responseText;
            console.log(response);

            var response = JSON.parse(xhr.responseText);
            var result = document.getElementById("colorLightboard");
            result.innerHTML = "";
            console.log(result);
            for (var i = 0; i < response.length; i++) {
                var lightData = response[i];
                console.log(lightData.light);
                var displayLight = document.createElement("div");
                displayLight.style.backgroundColor = 'rgb(' + [lightData.light.red,lightData.light.green,lightData.light.blue].join(',') + ')';
                displayLight.style.width = "100px";
                displayLight.style.height = "100px";
                
                displayLight.style.float = "left";
                if (lightData.column === 5) {
                    result.append(displayLight);
                    var placeholder = displayLight.cloneNode(true);
                    placeholder.style.float = "none";
                    result.append(placeholder);
                } else {
                    result.append(displayLight);
                }
                

                
            }


          } else {
            // If the request was unsuccessful, display an error message
            alert('Request failed. Returned status of ' + xhr.status);
          }
        };
        xhr.send();
    }
</script>
