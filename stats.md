## Statistics

<!--No actions yet-->
<div class="stats">
  <div class="container">
    <div class="row">
      <div class="col-lg-4">
        <div class="card shadow-sm">
          <div class="card-header bg-transparent text-center">
            <h3>Card Set #1</h3>
          </div>
          <div class="card-body">
            <p class="mb-0"><strong class="pr-1">Number of Terms:</strong>23</p>
            <p class="mb-0"><strong class="pr-1">Date Completed:</strong>1/17/23</p>
            <p class="mb-0"><strong class="pr-1">Subject: </strong>CS</p>
            <p class="mb-0"><button type="button" id="retry-button">Retry</button></p>
          </div>
        </div>
      </div>
      <div class="col-lg-8">
        <div class="card shadow-sm">
          <div class="card-header bg-transparent border-0">
            <h3 class="mb-0"><i class="far fa-clone pr-1"></i>General Information</h3>
          </div>
          <div class="card-body pt-0">
            <table class="table table-bordered">
              <tr>
                <th width="30%">Previous Score</th>
                <td width="2%">:</td>
                <td>17/23</td>
              </tr>
              <tr>
                <th width="30%">High Score</th>
                <td width="2%">:</td>
                <td>21/23</td>
              </tr>
              <tr>
                <th width="30%">Most Missed</th>
                <td width="2%">:</td>
                <td>Constructor</td>
              </tr>
              <tr>
                <th width="30%">Most Correct</th>
                <td width="2%">:</td>
                <td>Class</td>
              </tr>
              <tr>
                <th width="30%">Time</th>
                <td width="2%">:</td>
                <td>3:23</td>
              </tr>
            </table>
          </div>
        </div>
          <div style="height: 26px"></div>
        <div class="card shadow-sm">
          <div class="card-header bg-transparent border-0">
            <h3 class="mb-0"><i class="far fa-clone pr-1"></i>Most Missed Card</h3>
          </div>
          <div class="card-body pt-0">
                <link rel="stylesheet" href="{{ '/assets/css/flashcard.css?v=' | append: site.github.build_revision | relative_url }}">
                <div class="flip-card" id="flipcard">
                    <div class="flip-card-inner" id="inner-flipcard" onclick="flipCard()">
                        <div class="flip-card-front">
                        Constructor
                        </div>
                        <div class="flip-card-back">
                            The first method that runs in a class before any other method. Allows for the initialization and declaration of variables so that way the variables can be used in the project
                        </div>
                    </div>
                </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>