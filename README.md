###Minimal Setup
Copy amaran folder in to your project folder.

It’s not required, but i recommend placing CSS files in ```<head>``` and JavaScript files and initialization code in the footer of your site (before the closing ```</body>``` tag).

```
<link rel="stylesheet" href="amaran/css/jquery.amaran.min.css">
<link rel="stylesheet" href="amaran/css/themes/all-themes.css">
```


jQuery required for **Amaran JS**.If you already have **jquery.js** on your site, don’t include it a second time, or use **jQuery.noConflict();** mode.

You can add jQuery via Google CDN

```
<script src="//ajax.googleapis.com/ajax/libs/jquery/1.10.2/jquery.min.js"></script>
```

Place Amaran JS after jQuery

```
<script src="amaran/js/jquery.amaran.js"></script>
```

So minimalistic setup look like this

```
<!DOCTYPE html>
<html>
<head>
    <title>My Web Page</title>
    <link rel="stylesheet" href="amaran/css/jquery.amaran.min.css">
    <link rel="stylesheet" href="amaran/css/themes/all-themes.css">
</head>
<body>
    <p>My Content</p>
    <script src="//ajax.googleapis.com/ajax/libs/jquery/1.10.2/jquery.min.js"></script>
    <script src="amaran/js/jquery.amaran.js"></script>
</body>
</html>
```

###Recomended Setup

I recommend Font Awesome Icons and Open Sans for better looking notifications.Specially for default theme.
Just place these two css files inside your ```<head>``` section.

```
<link href="//netdna.bootstrapcdn.com/font-awesome/4.0.3/css/font-awesome.css" rel="stylesheet">
<link href='http://fonts.googleapis.com/css?family=Open+Sans:400,600' rel='stylesheet' type='text/css'>
```
So recomended setup should look like this;

```
<!DOCTYPE html>
<html>
<head>
    <title>My Web Page</title>
    <link href="//netdna.bootstrapcdn.com/font-awesome/4.0.3/css/font-awesome.css" rel="stylesheet">
    <link href='http://fonts.googleapis.com/css?family=Open+Sans:400,600' rel='stylesheet' type='text/css'> 
    <link rel="stylesheet" href="amaran/css/jquery.amaran.min.css">
    <link rel="stylesheet" href="amaran/css/themes/all-themes.css">
</head>
<body>
    <p>My Content</p>
    <script src="//ajax.googleapis.com/ajax/libs/jquery/1.10.2/jquery.min.js"></script>
    <script src="amaran/js/jquery.amaran.js"></script>
</body>
</html>
```

###Basic Usage

We are ready to create our first example.Very very simple usage of Amaran JS.

First of all we must add our code inside jQuery document ready function.```$(function(){ });```

```
$(function(){
    $.amaran({'message':'My first example!'});
});    
```

If you add this code inside ```$(function(){ })``` function it will automatically popsup when page loads.

I know not funcy as demos lets create themed example.I will cover more about themes in next section.

```
$.amaran({
    content:{
        message:'My first funcy example!',
        size:'1.4 GB',
        file:'my_birthday.mp4',
        icon:'fa fa-download'
    },
    theme:'default ok'
});
```

Lets see full example.

```
<!DOCTYPE html>
<html>
<head>
    <title>My Web Page</title>
    <link href="//netdna.bootstrapcdn.com/font-awesome/4.0.3/css/font-awesome.css" rel="stylesheet">
    <link href='http://fonts.googleapis.com/css?family=Open+Sans:400,600' rel='stylesheet' type='text/css'>
    <link rel="stylesheet" href="amaran/css/jquery.amaran.min.css">
    <link rel="stylesheet" href="amaran/css/themes/all-themes.css">
</head>
<body>
    <p>My Content</p>
    <script src="//ajax.googleapis.com/ajax/libs/jquery/1.10.2/jquery.min.js"></script>
    <script src="amaran/js/jquery.amaran.js"></script>
    <script>
        $(function(){
            $.amaran({
                content:{
                    message:'Your Download is Ready!',
                    size:'1.4 GB',
                    file:'my_birthday.mp4',
                    icon:'fa fa-download'
                },
                theme:'default ok'
            });
        });
    </script>
</body>
</html>         
```

###Using Themes

We have currently 5 themes.Some of them have variations like "default" theme.Lets look at themes.

####default theme

Default theme has 7 variations.

// image will include here

Usage;

```
$.amaran({
    content:{
        message:'Your Download is Ready!',
        size:'1.4 GB',
        file:'my_birthday.mp4',
        icon:'fa fa-download'
    },
    theme:'default ok'
});
```

You can specify a theme by passing ```theme : ''``` option to Amaran JS object.

For "default" theme you can call theme and variation with theme ```'default <VARIATION NAME>'``` e.g : ```theme:'default ok'``` or ```theme:'default error'```

For "default" theme we have 3 content options message,size and file.message represent first line,size second line and file reperesent third line.

With icon options you can specify icon."default" theme using Font Awesome icons.Icons list can be found in this ```http://fontawesome.io/icons/``` adress.

e.g For envelope icon just pass ```icons:'fa fa-envelope'```

**Creating your own variations**

```
.amaran.default.<VARIATION NAME> p.bold{
    color:<COLOR CODE>;
}
.amaran.default.<VARIATION NAME> .icon {
    background-color:<COLOR CODE>;
    color:#fff;
}
```
