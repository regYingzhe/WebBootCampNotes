# WebBootCampNotes
<h2>Score Keeper Notes</h2>
1. To change inline text style:<return>
<p>First, create a css file with the specify class for that text: e.g .winningScore{color: green}</p>
<p>Second, apply the style to the text by using p1Display.classList.add("winningScore")<return></p>
2. To change inline Text content:<return>
<p>First, create a <span> tag for that inline Text and assign and id</p>
<p>Second, select that specific <span> tag by using querySelector</p>
<p>Third, using textContent or innerHTML to change the content under the span</p>
<p>Forth, to find out the input value, we could do first console.dir(tag), and we will see the value is a key this DOM</p>
3.To grab a change event on the input <return>
<p>First, select the input tag numInput = document.querySelector("Input")</p>
<p>Second, add an EventListener</p>

# jQuery Notes
1. How to Manipulating Style: $(someSelector).css(property, value)
2. you can create an object with multiple styles and apply the object as the value to jQuery. e.g. 
var styles= {color: "red", background: "pink", border: "2px solid purple"}, then
$('h1').css(styles)
3. with jQuery if we want to change all the styles that applied to li, we don't need to loop through each element 
like we did by using document.querySelectorAll('li'), just $('li').css('color', 'pink')
4. text() to show all the text content 
5. html() = innerHTML(), $('li').html('<li>I hacked your URL</li>'), don't mess up html and text. If we have a input test, and usr inject some js code or html code, we want to treat the code as text not html.
6. 

# Tip:
1.querySelector only select the first element. That's why querySelectorAll exist.
2.$() == querySelectorAll, $("li a") = to select all a tags inside of li's
3.
