The form element is a container element like div. It has two essential attributes, `method` and `action`. The `action` attribute takes in a URL which tells the form where it should send it's data to be processed. The second attribute `method` tells browser which HTTP request method it should use to submit the form. The most used ones are GET and POST. We use GET when we want to retrieve something from the server. Post is used when we want to change something on the server.
The markup to create a form looks like this:

```
<form action="example.com/path" method="post">

</form>
```

## Form controls

### The input element

The input element accepts a `type` attribute which tells the browser what type of data it should expect and how to render that input element.

```
<form action="example.com/path" method="post">
	<input type="text">
</form>
```

#### Labels

We can give labels to elements to inform the users what kind of data they should type in:

```
<form action="example.com/path" method="post">
	<label for="first_name">First Name:</label>
	<input type="text" id="first_name">
</form>
```

Labels accept a `for` attribute which associates it with a particular input. The input we want to associate with a label needs an `id` attribute with the same value as the label's `for` attribute. When a label associated with that input is clicked, it will focus on the input.

#### Placeholder attribute

To guide users on what to enter in form elements we can include a placeholder in our input fields:

```
<label for="first_name">First Name:</label>
<input type="text" id="first_name" placeholder="Bob...">
```

#### The name attribute

The name attribute is added so that the backend knows what each peace of data sent represents. 

```
<label for="first_name">First Name:</label>
<input type="text" id="first_name" name="first_name"> 
```

A form element should always have a `name` attribute, otherwise it will be ignored when submitted, you can think of this as a variable for the input.

#### The type attribute

`Email` inputs are specialised text inputs just for email addresses. They are different from text inputs, the email type input will have validation and will have a keyboard that will include @ on mobile devices.

`Password` inputs are another specialized text input. They differ from regular text inputs by masking the data with * or a bullet point to prevent anyone from seeing what has been inputted.

The `number` input only accepts number values and ignores any other characters the user tries to enter.

`date` type makes the user experience better by making the date choosing easier by rendering a date picker.

#### Text area

An area for text that spans multiple lines like user comments and reviews. It can also be resized by clicking and dragging the bottom right corner to make it bigger or smaller.

```
<textarea></textarea>
```

You can display some initial content like this:

```
<textarea>Some initial content</textarea>
```

`row` and `cols` attributes allow you to control initial height(rows) and width(cols) of the text area:

```
<textarea rows="20" cols="60"></textarea>
```

### Selection elements

#### Select dropdown