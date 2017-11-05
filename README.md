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
4.##### How to add a post route: From the get route form submit post to the post route, in the restful convention, the post route name ##### should be same with the get route name which displays everything
`var fruit = [apple, waterMelon];`
`app.post("/addfruit", function(req, res) { var newFruit = req.body.newfruit; fruit.push(newFruit); res.redirect("/fruit")});
 app.get("/fruit", function(req, res) { res.render("fruit", {fruit: fruit})})`, 
 then use form to make post request. Inside EJS fruit,
`<form action="/addfruit" methos="POST">
	<input type="text" placeholder="fruit" name="newFruit"></input>
	<button>Submit</button>
 </form>`


# jQuery Notes
1. How to Manipulating Style: $(someSelector).css(property, value)
2. you can create an object with multiple styles and apply the object as the value to jQuery. e.g. 
var styles= {color: "red", background: "pink", border: "2px solid purple"}, then
$('h1').css(styles)
### All of these funtions combine the getter and setter relationship, provide one argument, it will become a getter, provide two args, it will become a setter method
3. with jQuery if we want to change all the styles that applied to li, we don't need to loop through each element 
like we did by using document.querySelectorAll('li'), just $('li').css('color', 'pink')
4. text() to show all the text content, e.g. $("ul").text() will give me all the text inside "li". Still, it will be convinient to change all the text all at once.
5. html() = innerHTML(),` $('li').html('<li>I hacked your URL</li>')`, don't mess up html and text. If we have a input test, and usr inject some js code or html code, we want to treat the code as text not html.
6. `$('img').attr("src", "html")` to set, `$("img").attr("src")` to get the information
7. `$('select').val()` to get the value from the dropdown menu
8. `$('input').val()` to retrieve the value from the input bar
9. `$('ul').addClass("correct")`, `$('li').last.toggleClass("correct")`, `$('li').last.removeClass("correct")`
10. click() method is a quick and easy way to add a click listener to element(s). `$("#submit").click(function() {})`, `$("button").click(function () {})`
11. `$("button").click(function() {$(this).css("background", "green")})` what happens behind the senses is we loops through each html element with tag button, and add click listener to each button. In vanilla html, we can use this to access the instance of the button that we click on, but in jQuery, we need to use $(this)
12. `$("input").keypress(function(event) {
	if(event.which == 13) {
	console.log("You pressed Enter")
}
})` keypress function can know which key you got pressed because each key encoded by a number in javascript.
13. 90% of the time, we will use on listener. `$("h1").on("click", function() {$(this).css("color", "purple")})`, mouseenter event: when hover over a button, the text will become bold for example. `$("button").on("mouseenter", function () { $(this).css("font-weight", "bold")})`, mouseleave: when mouse leave the button, the text will become normal
14. 

# EJS
1. npm install ejs --save
2. mkdir views; cd views; touch home.ejs
3. <% javaScript code %>, <%= %> output the result to the html. <%%> for logic, like loop and condition
4. `<li><%= posts[i].title %> - <strong><%= posts[i].author%></strong></li>`
5. mkdir public; cd public; touch app.css; then let express use the css files inside public folder: app.use(express.static("public"))
6. `<% campgrounds.forEach(function(campground) { %>
    <div>
        <h4><%= campground.name%></h4>
    </div>
<% }); %>`

# Tip:
1.querySelector only select the first element. That's why querySelectorAll exist.
2.$() == querySelectorAll, $("li a") = to select all a tags inside of li's
3.
4
