1.  Difference between LiveServer vs reveal in browser

    http://127.0.0.1:5500/test/index.html vs file:///D:/HtmlCss/test/index.html

2.  Html structure

        <!DOCTYPE html>
        <html lang="en">
        <head>
        </head>
        <body>
        </body>
        </html>

3.  settings => Open settings (JSON) [vscode settings]
    e.g. word wrap => off (no line break)

4.  Html is white space collapsing (ignore empty spaces including changing line and duplicate space between words)

5.  Lorem Ipsum => <p>lorem5</p>(output 5 words)

6.  [html attribute](https://www.google.com/url?sa=i&url=http%3A%2F%2Fweb.simmons.edu%2F~grabiner%2Fcomm244%2Fweekone%2Fhtml-attributes.html&psig=AOvVaw1cVpqlXBIP-l1Q--csWulS&ust=1676772471656000&source=images&cd=vfe&ved=2ahUKEwjD3c2t_p39AhXUkFYBHVEmAOwQjRx6BAgAEAo)

    attribute = attribute name + attribute value

7.  Relative path (important add ./) => ./images/girl2.jpg
8.  Copyright free images => pexels, pixabay, gratisography
9.  The Anchor element => external links, internal links, same page

10. href="#" details=> https://stackoverflow.com/questions/4855168/what-is-href-and-why-is-it-used
11. Download prettier extension
    setting => Search format => 1. Default Formatter=prettier 2. Format on Paste and Format on Save (check all)
12.     <br/> (useful): change line
13. Label is not essential in form
14. Label for and input id can be a pair or Label for and select id can also be a pair

<br/>

<hr/>

         <h1></h1>
         <p></p>
         <img src="./images/girl2.jpg" alt="girl2.jpg" width="500"/>
         <!--comment-->

<hr/>

         External: <a href="https://www.google.com.tw/" target="\_blank">navigate here</a>
         Internal: <a href="./about.html">about me</a>
         Page: <a href="#qq"></a>

<hr/>

         <sup></sup>

         <sub></sub>

         <strong></strong>

         <em></em>

<hr/>
List example:

         <ul>
         <li>gz</li>
         <li>js</li>
         </ul>

         <ol>
         <li>gz</li>
         <li>js</li>
         </ol>

<hr/>
Table example:
        
         <table>
         <tr>
         <th>Girl</th>
         <th>Tel</th>
         </tr>
         <tr>
         <td>Judy</td>
         <td>123</td>
         </tr>
         <tr>
         <td>Cloudia</td>
         <td>456</td>
         </tr>
         </table>

<hr/>
Simple Form example:

         <form action="">
            <label for="firstName">Firstname:</label>
            <input type="text" id="firstName" name="first" />
            <br />
            <label for="password">Password</label>
            <input
            type="password"
            id="password"
            name="second"
            placeholder="Please type password"
            autocomplete="on"
            />
            <br />
            <label for="email">Email</label>
            <input type="email" id="email" name="third" value="email@google.com" />

            <input type="submit" value="submit here" />
         </form>

<hr/>
Simple Form example adding ratio:

    <form action="">



      <p>Your favorite language</p>
      <p>[Label + input]</p>
      <input
        type="radio"
        name="fifth"
        id="coding1"
        value="javascript"
        checked
      />
      <label for="coding1">Javascript</label>
      <input type="radio" name="fifth" id="coding2" value="python" />
      <label for="coding2">python</label>
      <input type="radio" name="fifth" id="coding3" value="golang" />
      <label for="coding3">Golang</label>
      <br />
      <br />
      <label for="description">Description</label>
      <textarea name="fourth" id="description" cols="30" rows="10"></textarea>
      <br />
      <br />
    </form>

<hr/>

Simple Form example adding checkbox:

<p>Without Label [if no label tag, the id attribute will be empty]</p>

    <form action="">
      <p>Your favorite language</p>

      <input
        type="checkbox"
        name="sixth"
        value="javascript"
        checked
      />Javascript <input type="checkbox" name="sixth" value="python" />python
      <input type="checkbox" name="sixth" value="golang" />golang
      <br />
      <br />
    </form>

<hr/>

Simple Form example adding select:

<p>[Label + select id]</p>

    <form action="">
      <label for="language">Your favorite language</label>
      <select name="seventh" id="language">
        <option value="javascript">Javascript</option>
        <option value="python">Python</option>
        <option value="golang">Golang</option>
      </select>
      <br />
      <br />
      <input type="submit" value="submit here" />
    </form>

<hr/>
