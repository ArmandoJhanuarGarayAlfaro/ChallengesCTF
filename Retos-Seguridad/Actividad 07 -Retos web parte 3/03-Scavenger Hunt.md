# Scavenger Hunt

## Descripcion
There is some interesting information hidden around this site [http://mercury.picoctf.net:44070/](http://mercury.picoctf.net:44070/). Can you find it?

## Pistas
You should have enough hints to find the files, don't run a brute forcer.

## Solucion 
```html
<!doctype html>
<html>
  <head>
    <title>Scavenger Hunt</title>
    <link href="[https://fonts.googleapis.com/css?family=Open+Sans|Roboto](view-source:https://fonts.googleapis.com/css?family=Open+Sans|Roboto)" rel="stylesheet">
    <link rel="stylesheet" type="text/css" href="[mycss.css](view-source:http://mercury.picoctf.net:44070/mycss.css)">
    <script type="application/javascript" src="[myjs.js](view-source:http://mercury.picoctf.net:44070/myjs.js)"></script>
  </head>

  <body>
    <div class="container">
      <header>
		<h1>Just some boring HTML</h1>
      </header>

      <button class="tablink" onclick="openTab('tabintro', this, '#222')" id="defaultOpen">How</button>
      <button class="tablink" onclick="openTab('tababout', this, '#222')">What</button>

      <div id="tabintro" class="tabcontent">
		<h3>How</h3>
		<p>How do you like my website?</p>
      </div>

      <div id="tababout" class="tabcontent">
		<h3>What</h3>
		<p>I used these to make this site: <br/>
		  HTML <br/>
		  CSS <br/>
		  JS (JavaScript)
		</p>
	<!-- Here's the first part of the flag: picoCTF{t -->
      </div>

    </div>

  </body>
</html>
```

```css
div.container {
    width: 100%;
}

header {
    background-color: black;
    padding: 1em;
    color: white;
    clear: left;
    text-align: center;
}

body {
    font-family: Roboto;
}

h1 {
    color: white;
}

p {
    font-family: "Open Sans";
}

.tablink {
    background-color: #555;
    color: white;
    float: left;
    border: none;
    outline: none;
    cursor: pointer;
    padding: 14px 16px;
    font-size: 17px;
    width: 50%;
}

.tablink:hover {
    background-color: #777;
}

.tabcontent {
    color: #111;
    display: none;
    padding: 50px;
    text-align: center;
}

#tabintro { background-color: #ccc; }
#tababout { background-color: #ccc; }

/* CSS makes the page look nice, and yes, it also has part of the flag. Here's part 2: h4ts_4_l0 */
```

User-agent: *
Disallow: /index.html
 Part 3: t_0f_pl4c
 I think this is an apache server... can you Access the next flag?
 
 ![visible en Github](https://github.com/Alexlife2002003/ChallengesCTF/blob/main/Retos-Seguridad/Actividad%2007%20-Retos%20web%20parte%203/Pasted%20image%2020230317171218.png)
![[Pasted image 20230317171218.png]]

![visible en Github](https://github.com/Alexlife2002003/ChallengesCTF/blob/main/Retos-Seguridad/Actividad%2007%20-Retos%20web%20parte%203/Pasted%20image%2020230317171338.png)
![[Pasted image 20230317171338.png]]
## Bandera
picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_7a46d25d}

## Notas Adicionales 

