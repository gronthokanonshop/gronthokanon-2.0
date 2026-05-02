let cart = [];

function addToCart(name, price){
cart.push({name,price});
document.getElementById("count").innerText = cart.length;
updateCart();
}

function openCart(){
document.getElementById("cartBox").style.display="block";
updateCart();
}

function closeCart(){
document.getElementById("cartBox").style.display="none";
}

function updateCart(){

let box = document.getElementById("cartItems");
box.innerHTML="";

let total=0;

cart.forEach(i=>{
box.innerHTML += `<p>${i.name} - ৳${i.price}</p>`;
total += i.price;
});

document.getElementById("total").innerText = total;
}

function checkout(){

let msg="নতুন অর্ডার:\n\n";
let total=0;

cart.forEach(i=>{
msg += `${i.name} - ৳${i.price}\n`;
total += i.price;
});

msg += "\nTotal: ৳"+total;

let url="https://wa.me/8801516595762?text="+encodeURIComponent(msg);

window.open(url,"_blank");

cart=[];
document.getElementById("count").innerText=0;
}

function searchBook(){
let input=document.getElementById("search").value.toLowerCase();
let items=document.querySelectorAll(".product");

items.forEach(item=>{
let name=item.getAttribute("data-name").toLowerCase();

if(name.includes(input)){
item.style.display="block";
}else{
item.style.display="none";
}
});
}
