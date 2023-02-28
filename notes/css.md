1.  selector {property1:value1;property2:value2}
2.  Vscode Extension (optional) => 1. Indent Rainbow 2.Auto Rename Tag 3. Highlighting Matching Tag
3.  Inline Css

        e.g. <h1 style="color:blue;font-size:50px;">

4.  Internal Css

        e.g. add <style>h1{color:blue;font-size:50px;}</style> in head tag

5.  External Css

        e.g. <link rel="stylesheet" href="./index.css" />

6.  Power struggle: last rule principle is often use for overwritting (it will only replace the specific property)
7.  Element Selectors:

        e.g. h1{color:blue;font-size:50px;}

8.  Grouping Selectors:

        e.g. h1,h2{color:blue;}

9.  ID Selectors:

        e.g. #title{color:blue;background:black;}

10. Class Selectors

        e.g. .blue{color:blue;background:black;}
        e.g. class="green uppercase"
        e.g. class="card card-1" (apply the last rule method, card is for the general settings)

11. div and span (Due to inheritance)

        DIV - used to group multiple elements (add the style of all at the same time )
        SPAN - used to group inline content

12. Inheritance: some properties are not inherited such as border,
13. (a) Specifity > last rule (b)Universal Selector e.g. \*{color:brown}

        e.g.
        .hero span {
        color: #ef4036;
        font-size: 60px;
        }

        .hero span {
        font-size: 300px;
        }

14. Combine selectors

    e.g.desendant selector (suggestion): .container p{color:blue;background:black;}

15. Direct children selector

    e.g. div > h1 {:}

16. First-line and First-letter
    e.g. p::first-line

17. :hover
    e.g. div:hover{color:green}

18. Link pseudo-class
    e.g. a:link {}(with hred),a:visited {},a:hover {},a:active {}

19. :root{} #the higher specifity
    e.g.
    :root{
    font-size:10px
    }

            .relative{
                    font-size:1.5rem
            }

    <hr/>
    Css colors

            Css colors: color,background(has two option : color or image),background-color

<hr/>
Css units

        Css units:
        properties: font-size, width, height,
        values:
        - px,
        - %(depend on parent,no default),
        - em(depend on parent,default=16px),
        - rem(depend on root (html tag),default=16px)
                e.g.
                        html{font-size:10px}
                        .relative{font-size:2rem} => 20pixels
        - vh,vw (prefered)
                e.g.
                        .hero{height:100vh;width:100vw}
                        .about{height:43vh;width:43vw} only we start scrolling this will be appear
        - calc
                e.g.
                        * {
                                margin: 0;
                        }
                        .navbar {
                                background: blue;
                                height: 6rem;
                                color: white;
                                font-size: 3rem;
                        }
                        .banner {
                                background: red;
                                height: calc(100vh - 6rem);
                        }
        - overflow and min-height:
                e.g.

                        .banner {
                                background: red;
                                min-height: calc(100vh - 6rem);(if the content is lot more than expected, min-height will be ideal)
                        }
                        .example{
                                background: green;
                                width:10rem;
                                height:25rem;(remind: height default is auto [according to your content])
                                overflow:hidden;(hide all the remain content)
                                overflow:scroll;(add scroll bar)
                        }
        - max-width:
                Card width control use max-width

<hr/>
 Css Typography

        Css Typography:
        text-transform,
        font-family,
        line-height (distance between two lines),
        font-size,
        font-weight(normal=400,bold=700),
        font-style,
        text-align,
        text-indent,
        letter-spacing(distance between two letters),
        word-spacing(distance between two words), text-decoration
        e.g.

        body {
                font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
        }

        ------------------------

        body {
                font-size:20px;
                line-height:1.5;
        }#for body we have line-height:30px

        h1 {
                font-size:40px
        } #for h1 we have line-height:60px

        ------------------------

        a {
                text-decoration: none; #underline
        }

        Note. if using google font, suppose use choose roboto:400, then css {font-weight:400} is only available

<hr/>
Css Box model:

                properties:
                padding,
                margin,
                {border:width,style,color},
                border-radius,
                {outline:width,style,color},
                {outline-offset:Xpx},
                Note: negative margin
                Note: border hack techinique e.g. * {border:2px solid red;}
                Note: text-align:center vs margin:3rem auto

<hr/>
Css Display property:

                e.g. block: h1,div,p
                e.g. inline: span,img,

                properties:
                {display:inline}
                {display:block}
                {display:inline-block}
                {display:none} # remove

                {box-sizing:border-box}

                {opacity:0~1} # hide
                {visibility:visible} # hide


                Note: Only block respects width/height, top/bottom margin, inline elements will not (Solution: {display:block})
                Note: {text-align:center} can be used in inline, but {width:px;margin:0 auto} needs to be used in block for centering
                Note: Block-level elements respect both horizontal and vertical margins whereas inline-level elements only respect horizontal margins.
                Note: ul li {list-style-type:none}
                Note: navbar with anchor element, we need to turn anchor to block element
                Note: {display:inline-block} does not start a new line and respect width/height, top/bottom margin
                Note: only {display:none} remove the element
                Note: according to section components example:
                        1. section title and section content use seperate div
                        2. section content be aware of big screen and small screen. Also control the width (max-width) of div to be stable: .section-center { width: 90vw; margin: 0 auto;max-width: 1170px;}
                        3. According above two, we dont need to specify the width of section(it covers all ony need to check the width of section content to be aligned), same as nav and hero

<hr/>
Css Background Images:

                properties:
                {background:url("relative path")}
                {background-repeat:no-repeat} # mostly used
                {background-size:cover} # mostly used (cover all)
                {background-position: center}  # mostly used, show the center of the img for big images, display the image on the center for small image
                {background-attachment:fixed} # the backround image will not be affected
                {background:linear-gradient(to top, blue,green)} # background transitions (from blue to green)
                {background:linear-gradient(315deg, blue,green)}
                {background:linear-gradient(rgba(0,0,0,0.2), rgba(0,0,0,0.9))}
                {background:linear-gradient(to top,rgba(0,0,0,0.5), rgba(0,0,0,0.5)),url("relative path")}

                shorcut: {background:linear-gradient(to top,rgba(0,0,0,0.5), rgba(0,0,0,0.5)),url("relative path") center/cover no-repeat fixed}


                Note:
                1. {background-repeat:repeat} is default
                2. {background-repeat:repeat-x,no-repeat(only this value does not repeat),space,round(will consider if there is enough spaces)} is default
                3. {background-size:contain} (keep the ratio of the image, if necessary we add img)
                4. {background-position: x% y%}
                5. {background-attachment:scroll}
                6. Additional: place text in the center of background image (use flexbox)
                7.
                .hero {
                        background: linear-gradient(
                        to right,
                        rgba(105, 62, 27, 0.5),
                        rgba(105, 62, 27, 1)
                        ),
                        url("./hero-bcg.jpg") center/cover;
                        min-height: calc(100vh - 5rem);
                } # covers all

                .hero-center {
                        width: 90vw;
                        max-width: 1170px;
                        margin: 0 auto;
                        padding: 5rem 0;
                        color: #fff;
                } # better looking

                .hero-center p {
                        margin-bottom: 1.5rem;
                        max-width: 35em; # last rule principle(overwrite)
                }
                8. em is according font-size according parent

<hr/>
Css Positions:

                properties:
                {float:left} # taking this element out of the normal flow, the following elements will be around it
                {clear:both} # reject to be around it (create a seperate new line for the element)
                {position:static} #default (always positioned according to the normal flow)
                {position:relative;left:20%} shift 20% from the left from normal position # the next paragraph will not fill out the space

                {position:absolute;top:0;left:0;} # if no {position:relative;} exists in parents, it is relative to the body, otherwise position relative to the parent with  {position:relative;}# the next paragraph will fill out the space

                {position:fixed;top:0;left:0;} # relative to viewport screen  # the next paragraph will fill out the space


                {position:sticky;top:0} # From relative to stick, once the position is met, it sticks # the next paragraph will not fill out the space (in the flow)

                @media screen and (max-width:768px){
                        body{background:green};
                        .banner{};
                        ...
                }

                p::before{
                        content:"hello there"; #must
                        display:"block";
                        background:#22
                }

                # Greate example of resposive div image
                div {
                        width: 70vw;
                        background: red;
                }
                img {
                        width: 100%;
                        display: block; since
                }
                https://mor10.com/removing-white-space-image-elements-inline-elements-descenders/



                Note:
                1. Position absolute and fixed will use other content to fill out the space
                2. Difference between navbar sticky and fixed # https://stackoverflow.com/questions/19501919/difference-between-positionsticky-and-positionfixed
                3. Media Query: max-width means up to XX px the css will follow the media query css, min-width means starting from XX px the css will follow the media query css
                4. Media query follows the last principle rule
                5. z-index doesnt work on static
                6. ::before and ::after => these pseudo elements add elements before and after the content (image does not work since no content)
                https://www.google.com/imgres?imgurl=https%3A%2F%2Fwww.freecodecamp.org%2Fnews%2Fcontent%2Fimages%2F2021%2F08%2Fattribute-1.png&imgrefurl=https%3A%2F%2Fwww.freecodecamp.org%2Fnews%2Fwhat-is-html-definition-and-meaning%2F&tbnid=Knl7JCBDvODM_M&vet=12ahUKEwigxeKS8qv9AhWSet4KHdnQAVcQMygCegUIARDAAQ..i&docid=M2PJ8qBgxlmdqM&w=1200&h=628&q=html%20content%20meaning&ved=2ahUKEwigxeKS8qv9AhWSet4KHdnQAVcQMygCegUIARDAAQ
                7. https://www.w3schools.com/cssref/tryit.php?filename=trycss_inset(inset + absolute)
                8. Absolute + z-index+ before and after e.g. creative/beforeAfterImage
                9. Absolute + inset e.g. creative/HoverImageEffect
                10. {margin:0 auto} may not be in the center e.g. an example below

                .hero-center {
                        width: 90vw;
                        max-width: 1170px;
                        margin: 0 auto;
                        padding: 5rem 0;
                        color: #fff;
                        position: absolute; #keypoints
                        top: 50%;
                        left: 50%;
                        transform: translate(-50%, -50%);#keypoints
                        /* border: 2px solid red; */
                        text-align: center;
                }

                e.g. float example
                Suppose there are four div

                div{
                        height:200px;
                        width:50%;
                        float:right;
                }

<hr/>

Transform, Transition and Animation:  
Overview:  
transform: translate(), rotate(),scale(),skew()  
transition: (change over time)  
animation: change over time with more control

                Properties:
                (if using % in value, it will consider the width and height of its element)
                {transform:translate(x,y)}
                {transform:translateX()}  #positive value moves right
                {transform:translateY()}  #positive value moves down

                {transform:scale(1.2,1.5)}
                {transform:scaleX(0.5)} # the width of the element will divided by two
                {transform:scaleY(0.5)}

                {transform:rotate(20deg)} # the elemenyt will rotate 20 degree clockwise

                {transform:skew(20deg,20deg)}

                ################################
                adding hover in element:

                {
                        transition-property:background,border-radius;
                        transition-duration:4s,2s;
                        transition-delay:2s;
                        transition-timing-function: ease-in;
                }

                # the above can be simply to
                {
                        transition: background 4s 2s, border-radius 2s 2s;
                }

                or

                {
                        transition: all 4s ease-in 2s;
                }




                #########################
                without adding hover in element:

                .animation {
                        background: blue;
                        /* animation-name: move;
                        animation-duration: 10s;
                        animation-iteration-count: 3; */
                        animation: move 5s infinite;
                        animation-fill-mode:fowards; #the output (backwards or fowards)
                }

                @keyframes move {
                        0% {
                        transform: translateX(20px);
                        }
                        50% {
                        transform: translateX(100px);
                        background: red;
                        }
                        75% {
                        transform: translateX(-200px);
                        background: yellow;
                        }
                        100% {
                        transform: translateX(20px);
                        background: green;
                        }
                }

                #########################
                Compare it with animation

                .transition {
                        background: red;
                        transition: all 2s linear;
                }
                .transition:hover {
                        background: yellow;
                        border-radius: 50%;
                        transform: translateX(100px);
                }



                Note:
                1. How to center div: position absolute + top:50%,left:50% + translate(-50%,-50%)
                2. {transition: all(effect) 3s(duration) here(effect) 5s(delay)}
                3. effect:
                        ease(default:slow start=>fast=>slow end)
                        linear (same speed)
                        ease-in (slow start)
                        ease-out (slow end)
                        ease-in-out

                4. hover and transition is a good option
                5. animation adding opacity is a good option

<hr/>
Css variables

                Example:

                :root{
                        --primaryColor:#f15025
                }

                h1{
                        color:var(--primaryColor)
                }

                Note:
                1. https://www.30secondsofcode.org/articles/s/css-root-vs-html
                2. local variable have a greater priority than global variable

<hr/>
Font-awesome

1.  Three options using font awesome
    Download Host Yourself - Web Fonts in font-awesome
    Add <link rel="stylesheet" href="./fontawesome-free-6.0.0-web/css/all.css" /> or using cdn or svg

                 Properties:
                 1. {text-shadow:0px 0px 6px red;}
                 2. {box-shadow:0px 0px 6px red;}

<hr/>

Sementic elements:
https://rollerblade.tw/semantic-elements/
article: not connected with below and above content
section: strongly connected with below and above content
often section then article

<hr/>

{object-fit: cover} #preventing image being distort, the property is for image

<hr/>

:is() & :not()

nav h2:hover,header h2:hover, section h2:hover{color:red;}  
=> :is (nav,header,section) h2:hover{color:red;}

.special :not(h1) {color:red;}

<hr/>

hsl color value often used for a collections of color in modern website

<hr/>

use live server(five server) instead of live server

<hr/>

- Design from mobile to PC is much more easier
- rem is prefered in project
- padding is for creating space for the element while margin is for between elements
- {margin:0 auto} & {max-width: 1170px;} or {width: 85vw;} is for big div (not the most outside div) or element such as card
- Create a div outside if creating an transform scale (preventing overflow)
- tea-station e.g. product section is a good sample
- when using float: consider width and margin
- change text of the input .form-control::placeholder
- ransition and hover combination is not a must
- submit form without backend: formspree website

<hr/>

Flexbox (flex container + flex items)

        properties:
        (flex container)
        .container{display:flex}
        .container{display:inline-flex} # it takes only the space
        .container{flex-direction:row} # default
        .container{flex-direction:row-reverse} #flip all the element in opposite x axis direction
        .container{flex-direction:column}
        .container{flex-wrap:nowrap} # default
        .container{flex-wrap:wrap} # use it if flex container if cannot fill out all the flex items # without media query
        .container{flex-wrap:wrap-reverse} #flip all the element in opposite y axis direction
        .container{justify-content:flex-start} #default
        .container{justify-content:flex-end} # move all items to the end
        .container{justify-content:space-between}
        .container{justify-content:space-around} #each item has space, the space between the elements are double than the margin
        .container{justify-content:space-evenly}
        .container{justify-content:center}

        .container{align-items:stretch} # default
        .container{align-items:flex-start}
        .container{align-items:flex-end}
        .container{align-items:center}
        .container{align-items:base-line} #align if the items height are different

        .container{align-content:stretch} # default
        .container{align-content:flex-start}
        .container{align-content:flex-end}
        .container{align-content:center}
        .container{align-content:space-around}
        .container{align-content:space-between}
        .container{gap:1rem 2rem} #row distance column distance


        (flex item)

        .item {order:1} #all children have order 0 by default #the bigger the order, the end it will be

        .item {align-self:flex-end}

        .item {flex-grow:1} # it will grow, other remains the same

        .item2 {flex-grow:2} .item1 {flex-grow:1} # item2 will grow faster than 2

        .item2 {flex-shrink:1} #default shrink as it get smaller

        .item {flex-basis:150px}

        .item {flex: 1 0} #flex-grow flex-shrink flex-basis
        e.g. if there are four item .box {flex: 0 0 25%} # the div will always divided by four

        .container {
                display:flex;
                flex-wrap:wrap;
                justify-content:space-evenly;
        }

        .item {
                flex: 0 0 calc(25% - 1rem)
        } # same as gap






        Note:
        1. Creating a hero
        .hero {
                min-height:100vh;
                display:flex;
                justify-content:center;
                align-items:center;
        }
        h1 {
                text-transform:uppercase;
                font-size:60px;
                color:red;
        }
        2. align-items and align-content
        https://stackoverflow.com/questions/27539262/whats-the-difference-between-align-content-and-align-items#:~:text=align%2Dcontent%20manages%20the%20space,one%20line%2C%20they%20behave%20similarly.

        3. https://medium.com/@byron.skoutaris/flexbox-vs-grid-36d36ae0096e (flex is for one dimension [It is a one dimensional if there is a large div]])

<hr/>

Grid is for 2d dimension

        Properties:
        .container {display:grid;grid-template-columns:200px 300px} # create two columns with specific width
        .container {display:grid;grid-template-columns:200px auto} # the second column width is auto
        .container {display:grid;grid-template-rows:auto 5rem}

        .container {display:grid;grid-template-columns:1fr 1fr} # fraction use the available space while px not

        .container {display:grid;grid-gap:50px 100px} #grid-gap is absolete
        .container {display:grid;grid-column-gap:20px}

        .container {display:grid;gap:20px 5px;}


        Note:
        1. Example

        .container {
                min-height:100vh;
                display:grid;
                grid-template-columns:1fr 1fr; # fraction will calculate the available space
                grid-template-rows: 1fr 1fr 1fr 1fr;
                grid-gap: 50px 100px # important
        }

<hr/>
Good Styling:  
nice style: font-family:monospace
3:57
