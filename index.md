## Quiz Me


<style>

/* Create three equal columns that floats next to each other */
.column {
  float: left;
  width: 33.33%;
  padding: 10px;
  height: 300px; /* Should be removed. Only for demonstration */
}

/* Clear floats after the columns */
.row:after {
  content: "";
  display: table;
  clear: both;
}

.img {
  width: 30px;
  height: 30px;
}
</style>

<div class="row">
  <div class="column">
    <h3>Description:</h3>
     <p>Quiz Me is an online platform that makes studying and learning easier and more engaging for students. With a focus on flashcards and quizzes, students can study a wide range of school subjects and track their progress with detailed performance statistics. Our platform offers an interactive and customizable experience, allowing students to choose the subjects and topics they want to study and connect with other students for a supportive learning environment. Join Quiz Me today for a smarter way to study and achieve your academic goals.
       <br>
       Sample login credentials: <br> Email: sample@sample.com <br> Password: S@mpl3123
</p>
  </div>
  <div class="column">
    <img src="assets/img/logo12.png">
  </div>
  <div class="column">
    <h3>Subjects:</h3>
    <p>Math</p>
    <p>English</p>
    <p>Computer Science</p>
    <p>History</p>
    <p>Science</p>
    <p>More</p>
  </div>
</div>
