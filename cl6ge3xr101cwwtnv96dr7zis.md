## How to add a youtube video to the web page

If I give you a task in which you have to add an external YouTube URL or a PDF to your web page, How would you do it? If you do not know the answer, don't worry. We will be covering the answer in this article only. So the short answer is-

![iframe.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1659695876420/lr9Ze7CIj.jpg align="left")

## What is an iframe?

*iframe* is an HTML tag. "I" in iframe stands for inline. the inline frame tag lets you add a web page to the current web page in a rectangular region with a scrollbar and borders. the *iframe* tag is typically used for embedding third-party media, your own media, widgets, code snippets, or embedding third-party applets such as payment forms.



** Syntax:**

```

<iframe src="URL" title="description"></iframe>

```

Where the *src* attribute contains the URL of the third-party media.

### How do I embed a YouTube video on a website?

**Step 1-** Open [Visual Studio Code](https://code.visualstudio.com/) or your preferred IDE.

**Step 2- **Create a new file and save it with an extension of *.html*. for eg., *index.html *.

**Step 3-** Type the following code in your IDE.

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
   
</body>
</html>
```

**Step 4-** Insert an * iframe * tag between the *body* tags.

```

.

.

<body>

    <iframe> </iframe>

</body>

.

.

```

**Step 5-** Add the "src" attribute to the *iframe* tag.

```
<iframe src="URL" > </iframe>
```

**Step 6-** Copy the URL of the YouTube video you want to add and paste it into the *src* attribute.

**In this case: **

```

URL-https://www.youtube.com/watch?v=RdoJvf757qA

```

Here comes the interesting part.

**Step 7-** At this point, remove everything between *https://www.youtube.com/* and Video_ID *RdoJvf757qA* and add  "*/ embed/*". 

**In this case:**

```

https://www.youtube.com/embed/RdoJvf75qA

```
Add this URL in the "src" attribute.
```

<!DOCTYPE html>

<html lang="en">

<head>

    <meta charset="UTF-8">

    <meta http-equiv="X-UA-Compatible" content="IE=edge">

    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Document>

</head>

<body>

    <iframe src="https://www.youtube.com/embed/RdoJvf757qA "> </iframe>

    

</body>

</html>

```

Save it and open the file in the browser.

**Result: **

![Screenshot (9).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1659694436587/LjNQsDs5R.png align="left")

**Step 8- ** Set width and height.

```

<!DOCTYPE html>

<html lang="en">

<head>

    <meta charset="UTF-8">

    <meta http-equiv="X-UA-Compatible" content="IE=edge">

    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Document>

</head>

<body>

    <iframe src="https://www.youtube.com/embed/RdoJvf757qA" width="640" height="315"> </iframe>

    

</body>

</html>

```

tadaaa!!

![Screenshot (8).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1659694334270/1BH63Vdzl.png align="left")


This is all about adding a youtube video to the web page. hope it helps you.

Thank you :)





