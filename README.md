# WebBootCampNotes
<h2>Score Keeper Notes</h2>
1. To change inline text style:<return>
<p>First, create a css file with the specify class for that text: e.g .winningScore{color: green}</p>
<p>Second, apply the style to the text by using p1Display.classList.add("winningScore")<return></p>
2. To change inline Text content:<return>
<p>First, create a <span> tag for that inline Text and assign and id</p>
<p>Second, select that specific <span> tag by using querySelector</p>
<p>using textContent or innerHTML to change the content under the span</p>
3.To grab a change event on the input <return>
<p>First, select the input tag numInput = document.querySelector("Input")</p>
<p>Second, add an EventListener</p>
