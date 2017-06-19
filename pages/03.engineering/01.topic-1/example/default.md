---
title: 'Hello world'
published: true
---

# Dillinger

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

Dillinger is a cloud-enabled, mobile-ready, offline-storage, AngularJS powered HTML5 Markdown editor.

  - Type some Markdown on the left
  - See HTML in the right
  - Magic

# New Features!

  - Import a HTML file and watch it magically convert to Markdown
  - Drag and drop images (requires your Dropbox account be linked)


You can also:
  - Import and save files from GitHub, Dropbox, Google Drive and One Drive
  - Drag and drop markdown and HTML files into Dillinger
  - Export documents as Markdown, HTML and PDF

Markdown is a lightweight markup language based on the formatting conventions that people naturally use in email.  As [John Gruber] writes on the [Markdown site][df1]

> The overriding design goal for Markdown's
> formatting syntax is to make it as readable
> as possible. The idea is that a
> Markdown-formatted document should be
> publishable as-is, as plain text, without
> looking like it's been marked up with tags
> or formatting instructions.

This text you see here is *actually* written in Markdown! To get a feel for Markdown's syntax, type some text into the left window and watch the results in the right.

### Tech

Dillinger uses a number of open source projects to work properly:

* [AngularJS] - HTML enhanced for web apps!
* [Ace Editor] - awesome web-based text editor
* [markdown-it] - Markdown parser done right. Fast and easy to extend.
* [Twitter Bootstrap] - great UI boilerplate for modern web apps
* [node.js] - evented I/O for the backend
* [Express] - fast node.js network app framework [@tjholowaychuk]
* [Gulp] - the streaming build system
* [Breakdance](http://breakdance.io) - HTML to Markdown converter
* [jQuery] - duh

And of course Dillinger itself is open source with a [public repository][dill]
 on GitHub.

### Installation

Dillinger requires [Node.js](https://nodejs.org/) v4+ to run.

Install the dependencies and devDependencies and start the server.

```sh
$ cd dillinger
$ npm install -d
$ node app
```

For production environments...

```sh
$ npm install --production
$ npm run predeploy
$ NODE_ENV=production node app
```

### Plugins

Dillinger is currently extended with the following plugins. Instructions on how to use them in your own application are linked below.

| Plugin | README |
| ------ | ------ |
| Dropbox | [plugins/dropbox/README.md] [PlDb] |
| Github | [plugins/github/README.md] [PlGh] |
| Google Drive | [plugins/googledrive/README.md] [PlGd] |
| OneDrive | [plugins/onedrive/README.md] [PlOd] |
| Medium | [plugins/medium/README.md] [PlMe] |
| Google Analytics | [plugins/googleanalytics/README.md] [PlGa] |


### Development

Want to contribute? Great!

Dillinger uses Gulp + Webpack for fast developing.
Make a change in your file and instantanously see your updates!

Open your favorite Terminal and run these commands.

First Tab:
```sh
$ node app
```

Second Tab:
```sh
$ gulp watch
```

(optional) Third:
```sh
$ karma test
```
#### Building for source
For production release:
```sh
$ gulp build --prod
```
Generating pre-built zip archives for distribution:
```sh
$ gulp build dist --prod
```
### Docker
Dillinger is very easy to install and deploy in a Docker container.

By default, the Docker will expose port 80, so change this within the Dockerfile if necessary. When ready, simply use the Dockerfile to build the image.

```sh
cd dillinger
docker build -t joemccann/dillinger:${package.json.version}
```
This will create the dillinger image and pull in the necessary dependencies. Be sure to swap out `${package.json.version}` with the actual version of Dillinger.

Once done, run the Docker image and map the port to whatever you wish on your host. In this example, we simply map port 8000 of the host to port 80 of the Docker (or whatever port was exposed in the Dockerfile):

```sh
docker run -d -p 8000:8080 --restart="always" <youruser>/dillinger:${package.json.version}
```

Verify the deployment by navigating to your server address in your preferred browser.

```sh
127.0.0.1:8000
```

#### Kubernetes + Google Cloud

See [KUBERNETES.md](https://github.com/joemccann/dillinger/blob/master/KUBERNETES.md)


### Todos

 - Write MOAR Tests
 - Add Night Mode

License
----

MIT

<table border="1" bordercolor="#000000" cellspacing="0" width="100%" cellpadding="3">
  <tbody><tr>
    <td class="x">Solid</td>
    <td class="x">Specific Gravity</td>
    <td class="x">Young's Modulus    </td>
    <td class="x">Poissons Ratio</td>
    <td class="x">Thermal Conductivity</td>
    <td class="x">Melting Point     </td>
    <td class="x">Ultimate. Strength</td>
    <td class="x">Specific Heat</td>
  </tr>
    <tr>
    <td class="x">&nbsp;</td>
    <td class="x">&nbsp;</td>
    <td class="x">x10<sup>10 </sup>Pa </td>
    <td class="x">&nbsp;</td>
    <td class="x">W /m/K</td>
    <td class="x">Deg K </td>
    <td class="x">x10<sup>6 </sup>Pa</td>
    <td class="x">KJ/Kg/K</td>
  </tr>
  <tr>
    <td>Alumina</td>
    <td>3,9</td>
    <td>20-40</td>
     <td>0,24</td>
    <td>21</td>
    <td>2323</td>
    <td>140-200</td>
    <td>1,05</td>
  </tr>
   <tr>
    <td>Bone</td>
    <td>1,8</td>
    <td>2,8</td>
     <td>-&nbsp;</td>
    <td>&nbsp;</td>
    <td>&nbsp;</td>
    <td>~150</td>
    <td>0,8</td>
  </tr>
  <tr>
    <td>Brass</td>
    <td>8,45</td>
    <td>10,5</td>
    <td>0,35</td>
    <td>120</td>
    <td>1200</td>
     <td>330-550</td>
    <td>0,37</td>
  </tr>
  <tr>
    <td>Brick</td>
    <td>1,4-2,2</td>
    <td>1-5</td>
    <td>0,6</td>
    <td>0,4-0,8</td>
    <td>&nbsp;</td>
     <td>&nbsp;</td>
    <td>0,8</td>
  </tr>
  <tr>
    <td>Concrete</td>
    <td>2,4</td>
    <td>1,0-1,7</td>
    <td>0,1-0,2</td>
    <td>1,0-1,5</td>
     <td>&nbsp;</td>
    <td>&nbsp;</td>
    <td>1,1</td>
  </tr>
  <tr>
    <td>Constantan</td>
    <td>8,9</td>
    <td>16,3</td>
    <td>0,33</td>
    <td>22</td>
    <td>1593</td>
    <td>400-570</td>
    <td>0,41</td>
  </tr>
   <tr>
    <td>Diamond</td>
    <td>3,3</td>
    <td>120</td>
    <td>&nbsp;</td>
    <td>900</td>
    <td>~3820</td>
    <td>&nbsp;</td>
    <td>0,5</td>
  </tr>
  <tr>
    <td>Dry Ground</td>
    <td>~1,6</td>
    <td>&nbsp;</td>
    <td>&nbsp;</td>
    <td>&nbsp;</td>
    <td>&nbsp;</td>
    <td>&nbsp;</td>
    <td>&nbsp;</td>
  </tr>
  <tr>
    <td>Dural</td>
    <td>2,8</td>
    <td>7</td>
    <td>0,33</td>
    <td>150</td>
    <td>913</td> 
    <td>230-500</td>
    <td>0,9</td>
  </tr>
  <tr>
    <td>Glass</td>
    <td>2,4-3,5</td>
    <td>5-8</td>
    <td>0,2-0,27</td>
    <td>0,4-1,1</td>
    <td>~1373</td> 
    <td>30-90</td>
    <td>0,5-0,8</td>
  </tr>
  <tr>
    <td>Granite</td>
    <td>2,7</td>
    <td>4-7</td>
    <td>&nbsp;</td>
    <td>2-4</td> 
    <td>&nbsp;</td>
    <td>&nbsp;</td>
    <td>0,8</td>
  </tr>
  <tr>
    <td>Manganin</td>
    <td>8,5</td>
    <td>12,4</td>
    <td>0,33</td>
    <td>22</td>
    <td>1233</td> 
    <td>465</td>
    <td>0,4</td>
  </tr>
  <tr>
    <td>Mica</td>
    <td>2,8</td>
    <td>&nbsp;</td>
    <td>&nbsp;</td>
    <td>~0,5</td>
    <td>&nbsp;</td> 
    <td>&nbsp;</td>
    <td>0,84</td>
  </tr>
  <tr>
    <td>Nichrome(80/20)</td>
    <td>8,36</td>
    <td>18,6</td>
    <td>0,38</td>
    <td>13</td>
    <td>&nbsp;</td>
    <td>170-900</td>
    <td>0,43</td>
  </tr>
  <tr>
    <td>Nylon 6</td>
    <td>1,14</td>
    <td>0,1-0,25</td>
    <td>&nbsp;</td>
    <td>0,25-0,3</td>
    <td>473-493</td>    
    <td>70-85</td>
    <td>1,6</td>
  </tr>
  <tr>
    <td>Paper Dry</td>
    <td>~1,0</td>
    <td>&nbsp;</td>
    <td>&nbsp;</td>
    <td>0,06</td>
    <td>&nbsp;</td>  
    <td>&nbsp;</td>
    <td>&nbsp;</td>
  </tr>
  <tr>
    <td>Perspex</td>
    <td>1,2</td>
    <td>0,27-0,35</td>
    <td>&nbsp;</td>
    <td>0,2</td>
    <td>353-388</td> 
    <td>50-75</td>
    <td>1,45</td>
  </tr>
  <tr>
    <td>Phosphor Bronze</td>
    <td>8,92</td>
    <td>10</td>
    <td>0,38</td>
    <td>~75</td>
    <td>1323</td>
     <td>330-750</td>
    <td>0,38</td>
  </tr>
  <tr>
    <td>Polystyrene</td>
    <td>1,06</td>
    <td>0,25-0,4</td>
    <td>&nbsp;</td>
    <td>0,1</td>
    <td>353-378</td>
     <td>35-60</td>
    <td>1,3</td>
  </tr>
  <tr>
    <td>Polythene</td>
    <td>0,93</td>
    <td>0,01-0,1</td>
    <td>&nbsp;</td>
    <td>0,25-0,5</td>
    <td>338-403</td>  
    <td>7-38</td>
    <td>2,2</td>
  </tr>
  <tr>
    <td>PTFE</td>
    <td>2,2</td>
    <td>0,04-0,06</td>
    <td>&nbsp;</td>
    <td>0,23-0,270</td>
    <td>~600</td>  
    <td>17-28</td>
    <td>1,05</td>
  </tr>
  <tr>
    <td>PVC (plasticized)</td>
    <td>1,7 </td>
    <td>0,03 </td>
    <td>- </td>
    <td>0,16-0,19</td>
    <td>343-353 </td>  
    <td>0,15-35 </td>
    <td>-  </td>
  </tr>
  
  <tr>
    <td>PVC (rigid)</td>
    <td>1,3</td>
    <td> 0,34</td>
    <td>0,42</td>
    <td>0,19 </td>
    <td>373-433</td>  
    <td>35-55</td>
    <td> 0,88 </td>
  </tr>
  <tr>
    <td>Porcelain</td>
    <td>2,4</td>
    <td>&nbsp;</td>
    <td>&nbsp;</td>
    <td>0,8-1,85</td>
    <td>1823</td>  
    <td>&nbsp;</td>
    <td>1,1</td>
  </tr>
  <tr>
    <td>Quartz (Fibre)</td>
    <td>2,65</td>
    <td>7,3</td>
    <td>&nbsp;</td>
    <td>9</td>
    <td>2293</td> 
    <td>&nbsp;</td>
    <td>0,73</td>
  </tr>
  <tr>
    <td>Quartz (fused)</td>
    <td>2,2</td>
    <td>&nbsp;</td>
    <td>&nbsp;</td>
    <td>1,3</td>  
    <td>2293</td>
    <td>&nbsp;</td>
    <td>0,73</td>
  </tr>
  <tr>
    <td>Steel</td>
    <td>7,8</td>
    <td>21</td>
     <td>0,3</td>
    <td>50</td>  
    <td>1626-1733</td>
    <td>480</td>
    <td>0,45</td>
  </tr>
  <tr>
    <td>Rubber</td>
    <td>1,1 -1,2</td>
    <td>0,001-0,1</td>
    <td>0,46-0,49</td>
    <td>~0,15</td>
     <td>398</td>
    <td>14-40</td>
    <td>1,6</td>
  </tr>
  <tr>
    <td>Sandstone</td>
    <td>2,4</td>
     <td>&nbsp;</td>
    <td>&nbsp;</td>
    <td>1,1-2,3</td>
     <td>&nbsp;</td>
    <td>1</td>
    <td>0,9</td>
  </tr>
  <tr>
    <td>Timber</td>
    <td>0,4 -0,8</td>
    <td>0,8-1,3</td>
    <td>&nbsp;</td>
    <td>~0,15</td>   
    <td>&nbsp;</td>
    <td>20-110</td>
    <td>1,6</td>
  </tr>
  <tr>
    <td class="x">Solid</td>
    <td class="x">Specific Gravity</td>
    <td class="x">Young's Modulus    </td>
    <td class="x">Poissons Ratio</td>
    <td class="x">Thermal Conductivity</td>
    <td class="x">Melting Point     </td>
    <td class="x">Ultimate. Strength</td>
    <td class="x">Specific Heat</td>
  </tr>
   <tr>
    <td class="x">&nbsp;</td>
    <td class="x">&nbsp;</td>
    <td class="x">x10<sup>10 </sup>Pa </td>
    <td class="x">&nbsp;</td>
    <td class="x">W /m/K</td>
    <td class="x">Deg K </td>
    <td class="x">x10<sup>6 </sup>Pa</td>
    <td class="x">KJ/Kg/K</td>
  </tr>
</tbody></table>

**Free Software, Hell Yeah!**

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)


   [dill]: <https://github.com/joemccann/dillinger>
   [git-repo-url]: <https://github.com/joemccann/dillinger.git>
   [john gruber]: <http://daringfireball.net>
   [df1]: <http://daringfireball.net/projects/markdown/>
   [markdown-it]: <https://github.com/markdown-it/markdown-it>
   [Ace Editor]: <http://ace.ajax.org>
   [node.js]: <http://nodejs.org>
   [Twitter Bootstrap]: <http://twitter.github.com/bootstrap/>
   [jQuery]: <http://jquery.com>
   [@tjholowaychuk]: <http://twitter.com/tjholowaychuk>
   [express]: <http://expressjs.com>
   [AngularJS]: <http://angularjs.org>
   [Gulp]: <http://gulpjs.com>

   [PlDb]: <https://github.com/joemccann/dillinger/tree/master/plugins/dropbox/README.md>
   [PlGh]: <https://github.com/joemccann/dillinger/tree/master/plugins/github/README.md>
   [PlGd]: <https://github.com/joemccann/dillinger/tree/master/plugins/googledrive/README.md>
   [PlOd]: <https://github.com/joemccann/dillinger/tree/master/plugins/onedrive/README.md>
   [PlMe]: <https://github.com/joemccann/dillinger/tree/master/plugins/medium/README.md>
   [PlGa]: <https://github.com/RahulHP/dillinger/blob/master/plugins/googleanalytics/README.md>
