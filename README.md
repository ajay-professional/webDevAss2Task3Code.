# webDevAss2Task3Code.
/*//DOCUMENT OBJECT MODEL
//console.dir(document);
console.log(document.URL);
console.log(document.title);
console.log(document.domain);
//document.title="123";
console.log(document.doctype);
console.log(document.head);
console.log(document.body);
console.log(document.all);
console.log(document.all[10]);
console.log(document.forms);*/

/*//GETELEMENTBYID
console.log(document.getElementById("header-title"));
let head=document.getElementById("header-title");
head.textContent="UNIVERSE";
head.innerText="Cosmos";
head.style.borderBottom="solid 2px black";*/
let title=document.querySelectorAll(".title");
console.log(title[0]);
title[0].style.fontWeight="bold";
title[0].style.color="green";
//GET ELEMENT BY CLASS NAME
let items=document.getElementsByClassName("list-group-item");
items[2].style.backgroundColor="green";
for(let i=0;i<items.length;i++){
    items[i].style.fontWeight="bold";
}
//GET ELEMENT BY TAG NAME
let abc=document.getElementsByTagName("li");
abc[4].style.backgroundColor="blue";
abc[4].style.color="white";
let def=document.getElementsByClassName("li");
def[0].style.fontWeight="bold";

//querySelector
/*let alpha=document.querySelector('.list-group-item:nth-child(2)');
alpha.style.backgroundColor="green";
let beta=document.querySelector('.list-group-item:nth-child(3)');
beta.style.visibility="hidden";*/
//querySelectorAll
let gamma=document.querySelectorAll('.list-group-item');
gamma[1].style.color="green";
let odd=document.querySelectorAll('li:nth-child(odd)');
for(let i=0;i<odd.length;i++){
    odd[i].style.backgroundColor="green";
}
//Traversing the DOM
let a=document.querySelector("#items");
//parent node
/*console.log(a.parentNode);
a.parentNode.style.backgroundColor="lightblue";
console.log(a.parentNode.parentNode);
console.log(a.parentNode.parentNode.parentNode);*/
//parentElement
//console.log(a.parentElement);
//a.parentElement.style.backgroundColor="lightblue";
//console.log(a.parentElement.parentElement);
//console.log(a.parentElement.parentElement.parentElement);
//a.parentElement.parentElement.parentElement.style.backgroundColor="lightyellow";

//childNodes
//console.log(a.childNodes);

//children
/*console.log(a.children);
console.log(a.children[1]);
a.children[1].style.backgroundColor="yellow";*/

//firstChild
//console.log(a.firstChild);

//firstElementChild
//console.log(a.firstElementChild);
//a.firstElementChild.textContent="THE SPORTS";

//lastChild
//console.log(a.lastChild);

//lastElementChild
/*console.log(a.lastElementChild);
a.lastElementChild.textContent="THE POLITICS";*/

//nextSibling
//console.log(a.nextSibling);

//nextElementSibling
//console.log(a.nextElementSibling);

//previousSibling
//console.log(a.previousSibling);

//previousElementSibling
/*console.log(a.previousElementSibling);
a.previousElementSibling.style.color="brown";*/

//createElement
//create a div
var newdiv=document.createElement('div');
console.log(newdiv);
//class name
newdiv.className="alpha";
//id name
newdiv.id="beta";
//set attribute
newdiv.setAttribute("attr", "gamma");
//create a text node
var newDivText=document.createTextNode("Hello World");
newdiv.appendChild(newDivText);
console.log(newdiv);
var container=document.querySelector('header .container');
var h1=document.querySelector('header h1');
container.insertBefore(newdiv,h1);
/*var container1=document.querySelector('.list-group');
var df=container[0];
container.insertBefore(newdiv,df);*/
let parentNode=document.getElementById('items');
parentNode.innerHTML='<li class="list-group-item">Item 1</li><li class="list-group-item">Item 2</li><li class="list-group-item">Item 3</li><li class="list-group-item">Item 4</li><li class="li">Item 5</li>';
parentNode.innerHTML='<li>Hello world</li>' + parentNode.innerHTML;

