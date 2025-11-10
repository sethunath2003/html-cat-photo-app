# 🐱 Cat Photo App Tutorial - Step by Step

This tutorial will guide you through building the Cat Photo App from freeCodeCamp's Responsive Web Design certification.

## 📚 What You'll Build

By the end of this tutorial, you'll have created a complete Cat Photo App featuring:
- Images of cats
- Links to cat resources
- Lists of things cats love and hate
- A form for submitting cat photos
- Proper HTML structure and semantics

## 🎯 Learning Objectives

- Understanding HTML structure
- Working with headings and paragraphs
- Adding images with proper attributes
- Creating links
- Building lists (ordered and unordered)
- Creating forms with inputs
- Using semantic HTML elements

## 🚀 Getting Started

### Prerequisites
- A text editor (VS Code, Sublime Text, Notepad++, or even Notepad)
- A web browser (Chrome, Firefox, Safari, or Edge)
- Basic computer skills

### Step 1: Create Your Project Folder

1. Create a new folder on your computer named `cat-photo-app`
2. Open your text editor
3. Create a new file named `index.html` in the `cat-photo-app` folder

## 📝 Building the Cat Photo App

### Step 2: Set Up Basic HTML Structure

Add the following basic HTML structure to your `index.html`:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cat Photo App</title>
</head>
<body>

</body>
</html>
```

**What this does:**
- `<!DOCTYPE html>` declares this as an HTML5 document
- `<html lang="en">` sets the language to English
- `<head>` contains metadata about the page
- `<body>` contains the visible content

### Step 3: Add the Main Heading

Inside the `<body>` tag, add:

```html
<main>
    <h1>CatPhotoApp</h1>
</main>
```

**Save and open** your `index.html` in a browser to see your heading!

### Step 4: Add Cat Photos Section

Add this section below the `<h1>`:

```html
<section>
    <h2>Cat Photos</h2>
    <!-- TODO: Add link to cat photos -->
    <p>See more <a target="_blank" href="https://freecatphotoapp.com">cat photos</a> in our gallery.</p>
    <a href="https://freecatphotoapp.com"><img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg" alt="A cute orange cat lying on its back"></a>
</section>
```

**What's new:**
- `<section>` groups related content
- `<h2>` is a second-level heading
- `<!-- -->` is a comment (not visible on the page)
- `<p>` is a paragraph
- `<a>` creates a link
- `<img>` displays an image
- `alt` attribute describes the image for accessibility

### Step 5: Add Cat Lists Section

Add a new section for lists:

```html
<section>
    <h2>Cat Lists</h2>
    <h3>Things cats love:</h3>
    <ul>
        <li>cat nip</li>
        <li>laser pointers</li>
        <li>lasagna</li>
    </ul>
    <figure>
        <img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/lasagna.jpg" alt="A slice of lasagna on a plate">
        <figcaption>Cats <em>love</em> lasagna.</figcaption>
    </figure>
    
    <h3>Top 3 things cats hate:</h3>
    <ol>
        <li>flea treatment</li>
        <li>thunder</li>
        <li>other cats</li>
    </ol>
    <figure>
        <img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/cats.jpg" alt="Five cats looking around a field">
        <figcaption>Cats <strong>hate</strong> other cats.</figcaption>
    </figure>
</section>
```

**What's new:**
- `<h3>` is a third-level heading
- `<ul>` creates an unordered (bulleted) list
- `<ol>` creates an ordered (numbered) list
- `<li>` is a list item
- `<figure>` groups an image with its caption
- `<figcaption>` provides a caption for an image
- `<em>` emphasizes text (italic)
- `<strong>` strongly emphasizes text (bold)

### Step 6: Add Cat Form Section

Add the final section with a form:

```html
<section>
    <h2>Cat Form</h2>
    <form action="https://freecatphotoapp.com/submit-cat-photo">
        <fieldset>
            <legend>Is your cat an indoor or outdoor cat?</legend>
            <label><input id="indoor" type="radio" name="indoor-outdoor" value="indoor" checked> Indoor</label>
            <label><input id="outdoor" type="radio" name="indoor-outdoor" value="outdoor"> Outdoor</label>
        </fieldset>
        
        <fieldset>
            <legend>What's your cat's personality?</legend>
            <input id="loving" type="checkbox" name="personality" value="loving" checked>
            <label for="loving">Loving</label>
            <input id="lazy" type="checkbox" name="personality" value="lazy">
            <label for="lazy">Lazy</label>
            <input id="energetic" type="checkbox" name="personality" value="energetic">
            <label for="energetic">Energetic</label>
        </fieldset>
        
        <input type="text" name="catphotourl" placeholder="cat photo URL" required>
        <button type="submit">Submit</button>
    </form>
</section>
```

**What's new:**
- `<form>` creates a form for user input
- `action` attribute specifies where to send form data
- `<fieldset>` groups related form elements
- `<legend>` provides a title for a fieldset
- `<label>` labels an input element
- `<input>` creates various input fields
- `type="radio"` creates radio buttons (one selection)
- `type="checkbox"` creates checkboxes (multiple selections)
- `type="text"` creates a text input
- `name` attribute identifies the input
- `value` attribute specifies the submitted value
- `checked` attribute pre-selects an option
- `required` attribute makes a field mandatory
- `<button>` creates a submit button

### Step 7: Add Footer

Add a footer at the end, just before the closing `</main>` tag:

```html
<footer>
    <p>No Copyright - <a href="https://www.freecodecamp.org">freeCodeCamp.org</a></p>
</footer>
```

## ✅ Complete Code

Your complete `index.html` should look like this:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cat Photo App</title>
</head>
<body>
    <main>
        <h1>CatPhotoApp</h1>
        
        <section>
            <h2>Cat Photos</h2>
            <!-- TODO: Add link to cat photos -->
            <p>See more <a target="_blank" href="https://freecatphotoapp.com">cat photos</a> in our gallery.</p>
            <a href="https://freecatphotoapp.com"><img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg" alt="A cute orange cat lying on its back"></a>
        </section>
        
        <section>
            <h2>Cat Lists</h2>
            <h3>Things cats love:</h3>
            <ul>
                <li>cat nip</li>
                <li>laser pointers</li>
                <li>lasagna</li>
            </ul>
            <figure>
                <img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/lasagna.jpg" alt="A slice of lasagna on a plate">
                <figcaption>Cats <em>love</em> lasagna.</figcaption>
            </figure>
            
            <h3>Top 3 things cats hate:</h3>
            <ol>
                <li>flea treatment</li>
                <li>thunder</li>
                <li>other cats</li>
            </ol>
            <figure>
                <img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/cats.jpg" alt="Five cats looking around a field">
                <figcaption>Cats <strong>hate</strong> other cats.</figcaption>
            </figure>
        </section>
        
        <section>
            <h2>Cat Form</h2>
            <form action="https://freecatphotoapp.com/submit-cat-photo">
                <fieldset>
                    <legend>Is your cat an indoor or outdoor cat?</legend>
                    <label><input id="indoor" type="radio" name="indoor-outdoor" value="indoor" checked> Indoor</label>
                    <label><input id="outdoor" type="radio" name="indoor-outdoor" value="outdoor"> Outdoor</label>
                </fieldset>
                
                <fieldset>
                    <legend>What's your cat's personality?</legend>
                    <input id="loving" type="checkbox" name="personality" value="loving" checked>
                    <label for="loving">Loving</label>
                    <input id="lazy" type="checkbox" name="personality" value="lazy">
                    <label for="lazy">Lazy</label>
                    <input id="energetic" type="checkbox" name="personality" value="energetic">
                    <label for="energetic">Energetic</label>
                </fieldset>
                
                <input type="text" name="catphotourl" placeholder="cat photo URL" required>
                <button type="submit">Submit</button>
            </form>
        </section>
        
        <footer>
            <p>No Copyright - <a href="https://www.freecodecamp.org">freeCodeCamp.org</a></p>
        </footer>
    </main>
</body>
</html>
```

## 🎨 Testing Your Work

1. **Save** your `index.html` file
2. **Open** it in your web browser
3. **Test** all the features:
   - Click the links (they should open)
   - Try the radio buttons (only one should be selected at a time)
   - Try the checkboxes (multiple can be selected)
   - Type in the text input
   - Click the Submit button

## 🐛 Common Issues and Fixes

### Issue: Images don't show
- **Fix**: Check your internet connection (images are loaded from URLs)
- Make sure you copied the URLs exactly

### Issue: Links don't work
- **Fix**: Check that the `href` attributes are correct
- Make sure you included the `https://`

### Issue: Form doesn't submit
- **Fix**: This is normal! The form submits to a demo server
- You'll see a confirmation page if it works

### Issue: Page looks plain
- **Fix**: That's okay! This tutorial focuses on HTML structure
- You can add CSS later to make it look better

## 🎓 What You've Learned

Congratulations! You've built a complete HTML page and learned:
- ✅ HTML document structure
- ✅ Semantic HTML elements
- ✅ Working with text (headings, paragraphs)
- ✅ Adding images with alt text
- ✅ Creating links
- ✅ Building lists
- ✅ Creating forms with various input types
- ✅ Using labels for accessibility

## 🚀 Next Steps

Now that your Cat Photo App is complete:
1. Follow the [GitHub Pages Guide](./GITHUB_PAGES.md) to host it online
2. Customize it (add your own touches!)
3. Submit it to this repository following [CONTRIBUTING.md](../CONTRIBUTING.md)

## 💡 Optional Customizations

Want to make it your own? Try:
- Changing the text content
- Adding more list items
- Using different cat images
- Adding your own sections
- Changing form questions

Just remember: keep the basic structure intact for your submission!

## 📚 Additional Resources

- [freeCodeCamp HTML Course](https://www.freecodecamp.org/learn/2022/responsive-web-design/)
- [MDN HTML Reference](https://developer.mozilla.org/en-US/docs/Web/HTML)
- [W3Schools HTML Tutorial](https://www.w3schools.com/html/)

---

**Great job!** You're ready to host your app and contribute it to the repository! 🎉
