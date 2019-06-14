/*css_transform*/
body {
    cursor: url(../images/mouse_50_59.png), auto;
}
div {
    height: 200px;
    text-align: center;
}
.insideBox {
    color: blue;
    text-align: center;
    border: 8px red double;
    border-radius: 5px;
    background-color: gold;
}
.outsideBox {
    text-align: center;
    border: 5px blue dotted;
    border-radius: 5px;
    background-color: yellowgreen;
}
#oneOne {
    transform: rotate3d(0,0,0,0deg);
}
#oneTwo {
    transform: rotate3d(50,50,50,50deg);
}
#oneThree {
    transform: rotate3d(50,50,50,-50deg);
}
#twoOne {
    transform: translateX(0px);
}
#twoTwo {
    transform: translateX(-200px);
}
#twoThree {
    transform: translateX(200px);
}
#threeOne {
    position: relative;
    animation-name: threeOne;
    animation-duration: 4s;
    animation-iteration-count: infinite;
    animation-timing-function: linear;
}
@keyframes threeOne {
    0%   {transform: rotate(0deg); left:0px;}
    25%  {transform: rotate(90deg); left:157px}
    75% {transform: rotate(-90deg); left:-157px}
    100% {transform: rotate(0deg); left:0px}
}
