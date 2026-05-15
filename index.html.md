<!DOCTYPE html>  
  
<html lang="ar" dir="rtl">  
<head>  
<meta charset="UTF-8">  
<meta name="viewport" content="width=device-width, initial-scale=1.0">  
<title>Tempo D'or | ساعات فاخرة</title>  
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;1,400&family=Cairo:wght@300;400;500;600;700;900&display=swap" rel="stylesheet">  
<style>  
*, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }  
  
:root {  
–gold: #B8943F;  
–gold2: #D4AF6A;  
–gold3: #F0D090;  
–cream: #F8F3EA;  
–cream2: #EEE6D4;  
–dark: #0E0C08;  
–dark2: #1A1710;  
–dark3: #2A2518;  
–text: #3A3020;  
–text2: #6A5F40;  
–white: #FFFDF8;  
}  
  
html { scroll-behavior: smooth; }  
  
body {  
font-family: ‘Cairo’, sans-serif;  
background: var(–dark);  
color: var(–cream);  
overflow-x: hidden;  
cursor: none;  
}  
  
/* Custom Cursor */  
.cursor {  
width: 12px; height: 12px;  
background: var(–gold2);  
border-radius: 50%;  
position: fixed;  
top: 0; left: 0;  
pointer-events: none;  
z-index: 9999;  
transition: transform 0.15s ease, opacity 0.3s;  
mix-blend-mode: difference;  
}  
.cursor-ring {  
width: 36px; height: 36px;  
border: 1px solid var(–gold2);  
border-radius: 50%;  
position: fixed;  
top: 0; left: 0;  
pointer-events: none;  
z-index: 9998;  
transition: all 0.25s ease;  
opacity: 0.6;  
}  
  
/* Loader */  
#loader {  
position: fixed; inset: 0;  
background: var(–dark);  
z-index: 9000;  
display: flex;  
flex-direction: column;  
align-items: center;  
justify-content: center;  
gap: 20px;  
transition: opacity 0.8s ease, visibility 0.8s;  
}  
#loader.hide { opacity: 0; visibility: hidden; }  
.loader-logo {  
font-family: ‘Playfair Display’, serif;  
font-size: 2.5rem;  
color: var(–gold2);  
letter-spacing: 4px;  
animation: pulse 1.5s ease-in-out infinite;  
}  
.loader-bar {  
width: 200px; height: 2px;  
background: var(–dark3);  
border-radius: 2px;  
overflow: hidden;  
}  
.loader-fill {  
height: 100%;  
background: linear-gradient(90deg, var(–gold), var(–gold3));  
animation: load 2s ease forwards;  
}  
@keyframes load { from{width:0} to{width:100%} }  
@keyframes pulse { 0%,100%{opacity:1} 50%{opacity:0.5} }  
  
/* Navigation */  
nav {  
position: fixed; top: 0; left: 0; right: 0;  
z-index: 100;  
padding: 0 5%;  
height: 80px;  
display: flex;  
align-items: center;  
justify-content: space-between;  
background: linear-gradient(to bottom, rgba(14,12,8,0.95), transparent);  
backdrop-filter: blur(10px);  
border-bottom: 1px solid rgba(184,148,63,0.15);  
transition: all 0.3s;  
}  
nav.scrolled {  
background: rgba(14,12,8,0.98);  
height: 65px;  
border-bottom-color: rgba(184,148,63,0.3);  
}  
.nav-logo {  
font-family: ‘Playfair Display’, serif;  
font-size: 1.6rem;  
color: var(–gold2);  
letter-spacing: 2px;  
text-decoration: none;  
}  
.nav-logo span { color: var(–gold3); font-style: italic; }  
.nav-links {  
display: flex;  
gap: 35px;  
list-style: none;  
}  
.nav-links a {  
color: var(–cream2);  
text-decoration: none;  
font-size: 0.85rem;  
font-weight: 500;  
letter-spacing: 1.5px;  
text-transform: uppercase;  
transition: color 0.3s;  
position: relative;  
}  
.nav-links a::after {  
content: ‘’;  
position: absolute;  
bottom: -4px; left: 0; right: 0;  
height: 1px;  
background: var(–gold2);  
transform: scaleX(0);  
transition: transform 0.3s;  
}  
.nav-links a:hover { color: var(–gold3); }  
.nav-links a:hover::after { transform: scaleX(1); }  
.nav-cart {  
position: relative;  
background: none;  
border: 1px solid var(–gold);  
color: var(–gold2);  
padding: 8px 20px;  
cursor: pointer;  
font-family: ‘Cairo’, sans-serif;  
font-size: 0.85rem;  
letter-spacing: 1px;  
transition: all 0.3s;  
display: flex;  
align-items: center;  
gap: 8px;  
}  
.nav-cart:hover { background: var(–gold); color: var(–dark); }  
.cart-count {  
background: var(–gold3);  
color: var(–dark);  
border-radius: 50%;  
width: 20px; height: 20px;  
font-size: 0.7rem;  
font-weight: 700;  
display: flex;  
align-items: center;  
justify-content: center;  
}  
.nav-menu-btn {  
display: none;  
background: none;  
border: none;  
color: var(–gold2);  
font-size: 1.5rem;  
cursor: pointer;  
}  
  
/* Hero */  
.hero {  
min-height: 100vh;  
display: flex;  
align-items: center;  
justify-content: center;  
position: relative;  
overflow: hidden;  
background: radial-gradient(ellipse at center top, #2A2010 0%, #0E0C08 60%);  
}  
.hero-bg-pattern {  
position: absolute; inset: 0;  
background-image:  
radial-gradient(circle at 20% 50%, rgba(184,148,63,0.08) 0%, transparent 50%),  
radial-gradient(circle at 80% 20%, rgba(184,148,63,0.05) 0%, transparent 40%);  
pointer-events: none;  
}  
.hero-lines {  
position: absolute; inset: 0;  
background-image:  
repeating-linear-gradient(90deg, rgba(184,148,63,0.03) 0px, rgba(184,148,63,0.03) 1px, transparent 1px, transparent 80px),  
repeating-linear-gradient(0deg, rgba(184,148,63,0.03) 0px, rgba(184,148,63,0.03) 1px, transparent 1px, transparent 80px);  
pointer-events: none;  
}  
.hero-content {  
text-align: center;  
z-index: 2;  
padding: 0 20px;  
animation: heroReveal 1.2s ease 2.2s both;  
}  
@keyframes heroReveal {  
from { opacity:0; transform: translateY(40px); }  
to { opacity:1; transform: translateY(0); }  
}  
.hero-eyebrow {  
font-size: 0.75rem;  
letter-spacing: 8px;  
color: var(–gold);  
text-transform: uppercase;  
margin-bottom: 20px;  
}  
.hero-title {  
font-family: ‘Playfair Display’, serif;  
font-size: clamp(3rem, 8vw, 7rem);  
line-height: 1.1;  
color: var(–white);  
margin-bottom: 10px;  
}  
.hero-title em {  
color: var(–gold2);  
font-style: italic;  
display: block;  
}  
.hero-subtitle {  
font-size: clamp(1rem, 2vw, 1.3rem);  
color: var(–text2);  
font-weight: 300;  
letter-spacing: 3px;  
margin-bottom: 50px;  
}  
.hero-cta {  
display: inline-flex;  
align-items: center;  
gap: 15px;  
background: linear-gradient(135deg, var(–gold), var(–gold2));  
color: var(–dark);  
padding: 16px 45px;  
font-family: ‘Cairo’, sans-serif;  
font-size: 0.95rem;  
font-weight: 700;  
letter-spacing: 2px;  
text-decoration: none;  
text-transform: uppercase;  
transition: all 0.4s;  
clip-path: polygon(10px 0%, 100% 0%, calc(100% - 10px) 100%, 0% 100%);  
}  
.hero-cta:hover {  
transform: translateY(-3px);  
box-shadow: 0 20px 40px rgba(184,148,63,0.4);  
}  
.hero-watch-img {  
position: absolute;  
right: -5%;  
top: 50%;  
transform: translateY(-50%);  
width: 45vw;  
max-width: 600px;  
opacity: 0.12;  
pointer-events: none;  
animation: floatWatch 6s ease-in-out infinite;  
}  
@keyframes floatWatch {  
0%,100% { transform: translateY(-50%) rotate(-5deg); }  
50% { transform: translateY(-53%) rotate(-3deg); }  
}  
.hero-scroll {  
position: absolute;  
bottom: 40px;  
left: 50%;  
transform: translateX(-50%);  
display: flex;  
flex-direction: column;  
align-items: center;  
gap: 8px;  
color: var(–gold);  
font-size: 0.7rem;  
letter-spacing: 3px;  
text-transform: uppercase;  
animation: bounce 2s ease-in-out infinite;  
}  
.hero-scroll::after {  
content: ‘’;  
width: 1px;  
height: 50px;  
background: linear-gradient(to bottom, var(–gold), transparent);  
}  
@keyframes bounce { 0%,100%{transform:translateX(-50%) translateY(0)} 50%{transform:translateX(-50%) translateY(10px)} }  
  
/* Section Common */  
section { padding: 100px 5%; }  
.section-label {  
font-size: 0.7rem;  
letter-spacing: 8px;  
color: var(–gold);  
text-transform: uppercase;  
margin-bottom: 12px;  
}  
.section-title {  
font-family: ‘Playfair Display’, serif;  
font-size: clamp(2rem, 4vw, 3rem);  
color: var(–white);  
margin-bottom: 15px;  
line-height: 1.2;  
}  
.section-title em { color: var(–gold2); font-style: italic; }  
.section-desc {  
color: var(–text2);  
font-size: 1rem;  
font-weight: 300;  
max-width: 500px;  
line-height: 1.8;  
}  
.gold-line {  
width: 60px; height: 2px;  
background: linear-gradient(to right, var(–gold), transparent);  
margin: 20px 0;  
}  
  
/* Features */  
.features {  
background: var(–dark2);  
padding: 60px 5%;  
border-top: 1px solid rgba(184,148,63,0.1);  
border-bottom: 1px solid rgba(184,148,63,0.1);  
}  
.features-grid {  
display: grid;  
grid-template-columns: repeat(4, 1fr);  
gap: 1px;  
background: rgba(184,148,63,0.1);  
}  
.feature-item {  
background: var(–dark2);  
padding: 40px 30px;  
text-align: center;  
transition: background 0.3s;  
}  
.feature-item:hover { background: var(–dark3); }  
.feature-icon {  
font-size: 2rem;  
margin-bottom: 15px;  
display: block;  
}  
.feature-title {  
font-size: 0.9rem;  
font-weight: 700;  
color: var(–gold2);  
letter-spacing: 1px;  
margin-bottom: 8px;  
}  
.feature-desc {  
font-size: 0.8rem;  
color: var(–text2);  
line-height: 1.6;  
}  
  
/* Products */  
.products-section { background: var(–dark); }  
.products-header {  
display: flex;  
justify-content: space-between;  
align-items: flex-end;  
margin-bottom: 50px;  
flex-wrap: wrap;  
gap: 20px;  
}  
.filter-tabs {  
display: flex;  
gap: 5px;  
flex-wrap: wrap;  
}  
.filter-tab {  
padding: 8px 20px;  
background: none;  
border: 1px solid rgba(184,148,63,0.3);  
color: var(–text2);  
font-family: ‘Cairo’, sans-serif;  
font-size: 0.8rem;  
letter-spacing: 1px;  
cursor: pointer;  
transition: all 0.3s;  
}  
.filter-tab.active, .filter-tab:hover {  
background: var(–gold);  
border-color: var(–gold);  
color: var(–dark);  
}  
.products-grid {  
display: grid;  
grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));  
gap: 2px;  
background: rgba(184,148,63,0.08);  
}  
.product-card {  
background: var(–dark2);  
transition: all 0.4s;  
position: relative;  
overflow: hidden;  
cursor: pointer;  
}  
.product-card:hover { background: var(–dark3); transform: translateY(-4px); }  
.product-badge {  
position: absolute;  
top: 20px;  
right: 20px;  
background: var(–gold);  
color: var(–dark);  
font-size: 0.65rem;  
font-weight: 700;  
letter-spacing: 2px;  
padding: 5px 12px;  
text-transform: uppercase;  
z-index: 2;  
}  
.product-badge.new { background: var(–dark3); color: var(–gold2); border: 1px solid var(–gold); }  
.product-img-wrap {  
height: 260px;  
background: linear-gradient(135deg, #1A1710, #2A2518);  
display: flex;  
align-items: center;  
justify-content: center;  
position: relative;  
overflow: hidden;  
}  
.product-img-wrap::before {  
content: ‘’;  
position: absolute; inset: 0;  
background: radial-gradient(circle at 50% 50%, rgba(184,148,63,0.15), transparent 70%);  
}  
.watch-visual {  
width: 160px;  
height: 160px;  
border-radius: 50%;  
border: 3px solid;  
display: flex;  
align-items: center;  
justify-content: center;  
position: relative;  
transition: transform 0.6s ease;  
font-size: 3rem;  
}  
.product-card:hover .watch-visual {  
transform: rotate(20deg) scale(1.05);  
}  
.watch-visual::before {  
content: ‘’;  
position: absolute;  
inset: 8px;  
border-radius: 50%;  
border: 1px solid rgba(184,148,63,0.3);  
}  
.watch-visual::after {  
content: ‘’;  
position: absolute;  
width: 3px;  
height: 50px;  
background: currentColor;  
top: 15px;  
border-radius: 2px;  
transform-origin: bottom center;  
}  
.product-info { padding: 25px; }  
.product-category {  
font-size: 0.65rem;  
letter-spacing: 3px;  
color: var(–gold);  
text-transform: uppercase;  
margin-bottom: 8px;  
}  
.product-name {  
font-family: ‘Playfair Display’, serif;  
font-size: 1.2rem;  
color: var(–white);  
margin-bottom: 5px;  
}  
.product-desc {  
font-size: 0.8rem;  
color: var(–text2);  
line-height: 1.5;  
margin-bottom: 15px;  
}  
.product-footer {  
display: flex;  
align-items: center;  
justify-content: space-between;  
border-top: 1px solid rgba(184,148,63,0.1);  
padding-top: 15px;  
}  
.product-price {  
display: flex;  
flex-direction: column;  
}  
.price-old {  
font-size: 0.75rem;  
color: var(–text2);  
text-decoration: line-through;  
}  
.price-new {  
font-size: 1.3rem;  
font-weight: 700;  
color: var(–gold2);  
}  
.price-currency { font-size: 0.75rem; font-weight: 400; }  
.btn-add-cart {  
background: none;  
border: 1px solid var(–gold);  
color: var(–gold2);  
padding: 10px 18px;  
font-family: ‘Cairo’, sans-serif;  
font-size: 0.8rem;  
cursor: pointer;  
transition: all 0.3s;  
letter-spacing: 1px;  
display: flex;  
align-items: center;  
gap: 6px;  
}  
.btn-add-cart:hover {  
background: var(–gold);  
color: var(–dark);  
transform: scale(1.02);  
}  
.product-card:hover .btn-add-cart { background: var(–gold); color: var(–dark); }  
  
/* About */  
.about-section {  
background: var(–dark2);  
display: grid;  
grid-template-columns: 1fr 1fr;  
gap: 80px;  
align-items: center;  
}  
.about-visual {  
position: relative;  
height: 500px;  
}  
.about-circle {  
position: absolute;  
border-radius: 50%;  
border: 1px solid rgba(184,148,63,0.3);  
}  
.about-circle:nth-child(1) { inset: 0; }  
.about-circle:nth-child(2) { inset: 30px; border-color: rgba(184,148,63,0.5); }  
.about-circle:nth-child(3) { inset: 70px; background: radial-gradient(circle, rgba(184,148,63,0.1), transparent); }  
.about-center {  
position: absolute;  
inset: 0;  
display: flex;  
align-items: center;  
justify-content: center;  
font-size: 6rem;  
animation: spin 20s linear infinite;  
}  
@keyframes spin { from{transform:rotate(0deg)} to{transform:rotate(360deg)} }  
.about-stats {  
display: grid;  
grid-template-columns: 1fr 1fr;  
gap: 25px;  
margin-top: 40px;  
}  
.stat-box {  
border: 1px solid rgba(184,148,63,0.2);  
padding: 25px;  
background: var(–dark3);  
}  
.stat-number {  
font-family: ‘Playfair Display’, serif;  
font-size: 2.5rem;  
color: var(–gold2);  
display: block;  
}  
.stat-label {  
font-size: 0.75rem;  
color: var(–text2);  
letter-spacing: 2px;  
text-transform: uppercase;  
}  
  
/* Testimonials */  
.testimonials { background: var(–dark); }  
.testimonials-grid {  
display: grid;  
grid-template-columns: repeat(3, 1fr);  
gap: 2px;  
background: rgba(184,148,63,0.08);  
margin-top: 50px;  
}  
.testimonial-card {  
background: var(–dark2);  
padding: 40px 35px;  
transition: background 0.3s;  
}  
.testimonial-card:hover { background: var(–dark3); }  
.stars {  
color: var(–gold2);  
font-size: 0.9rem;  
letter-spacing: 3px;  
margin-bottom: 20px;  
}  
.testimonial-text {  
font-size: 0.95rem;  
color: var(–cream2);  
line-height: 1.8;  
font-style: italic;  
margin-bottom: 25px;  
font-family: ‘Playfair Display’, serif;  
}  
.testimonial-author {  
display: flex;  
align-items: center;  
gap: 12px;  
border-top: 1px solid rgba(184,148,63,0.1);  
padding-top: 20px;  
}  
.author-avatar {  
width: 45px; height: 45px;  
border-radius: 50%;  
background: linear-gradient(135deg, var(–gold), var(–dark3));  
display: flex;  
align-items: center;  
justify-content: center;  
font-size: 1.2rem;  
border: 1px solid rgba(184,148,63,0.3);  
}  
.author-name {  
font-size: 0.85rem;  
font-weight: 600;  
color: var(–white);  
}  
.author-loc {  
font-size: 0.75rem;  
color: var(–text2);  
letter-spacing: 1px;  
}  
  
/* Order Modal */  
.modal-overlay {  
position: fixed; inset: 0;  
background: rgba(0,0,0,0.85);  
z-index: 500;  
display: flex;  
align-items: center;  
justify-content: center;  
padding: 20px;  
opacity: 0;  
visibility: hidden;  
transition: all 0.3s;  
backdrop-filter: blur(8px);  
}  
.modal-overlay.open { opacity: 1; visibility: visible; }  
.modal {  
background: var(–dark2);  
border: 1px solid rgba(184,148,63,0.3);  
max-width: 550px;  
width: 100%;  
max-height: 85vh;  
overflow-y: auto;  
transform: translateY(30px);  
transition: transform 0.3s;  
}  
.modal-overlay.open .modal { transform: translateY(0); }  
.modal-header {  
padding: 30px 35px 20px;  
border-bottom: 1px solid rgba(184,148,63,0.15);  
display: flex;  
align-items: center;  
justify-content: space-between;  
}  
.modal-title {  
font-family: ‘Playfair Display’, serif;  
font-size: 1.5rem;  
color: var(–gold2);  
}  
.modal-close {  
background: none; border: none;  
color: var(–text2); font-size: 1.5rem;  
cursor: pointer; transition: color 0.2s;  
line-height: 1;  
}  
.modal-close:hover { color: var(–gold2); }  
.modal-body { padding: 30px 35px; }  
.modal-product-info {  
display: flex;  
align-items: center;  
gap: 20px;  
padding: 20px;  
background: var(–dark3);  
margin-bottom: 30px;  
border: 1px solid rgba(184,148,63,0.1);  
}  
.modal-watch-icon { font-size: 3rem; }  
.modal-product-name {  
font-family: ‘Playfair Display’, serif;  
font-size: 1.1rem;  
color: var(–white);  
}  
.modal-product-price {  
font-size: 1.3rem;  
font-weight: 700;  
color: var(–gold2);  
margin-top: 5px;  
}  
.form-group {  
margin-bottom: 20px;  
}  
.form-label {  
display: block;  
font-size: 0.8rem;  
letter-spacing: 2px;  
color: var(–gold);  
text-transform: uppercase;  
margin-bottom: 8px;  
}  
.form-input, .form-select, .form-textarea {  
width: 100%;  
background: var(–dark3);  
border: 1px solid rgba(184,148,63,0.2);  
color: var(–cream);  
padding: 12px 16px;  
font-family: ‘Cairo’, sans-serif;  
font-size: 0.9rem;  
outline: none;  
transition: border-color 0.3s;  
direction: rtl;  
}  
.form-input:focus, .form-select:focus, .form-textarea:focus {  
border-color: var(–gold2);  
}  
.form-select option { background: var(–dark3); }  
.form-textarea { resize: vertical; min-height: 80px; }  
.form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 15px; }  
.btn-submit {  
width: 100%;  
background: linear-gradient(135deg, var(–gold), var(–gold2));  
border: none;  
color: var(–dark);  
padding: 16px;  
font-family: ‘Cairo’, sans-serif;  
font-size: 1rem;  
font-weight: 700;  
letter-spacing: 2px;  
cursor: pointer;  
text-transform: uppercase;  
transition: all 0.3s;  
margin-top: 10px;  
}  
.btn-submit:hover {  
box-shadow: 0 10px 30px rgba(184,148,63,0.4);  
transform: translateY(-2px);  
}  
  
/* Cart Drawer */  
.cart-drawer {  
position: fixed;  
top: 0; left: 0;  
width: 400px;  
max-width: 100vw;  
height: 100vh;  
background: var(–dark2);  
border-right: 1px solid rgba(184,148,63,0.2);  
z-index: 600;  
transform: translateX(-100%);  
transition: transform 0.4s cubic-bezier(0.4,0,0.2,1);  
display: flex;  
flex-direction: column;  
}  
.cart-drawer.open { transform: translateX(0); }  
.cart-drawer-header {  
padding: 25px;  
border-bottom: 1px solid rgba(184,148,63,0.15);  
display: flex;  
align-items: center;  
justify-content: space-between;  
}  
.cart-drawer-title {  
font-family: ‘Playfair Display’, serif;  
font-size: 1.3rem;  
color: var(–gold2);  
}  
.cart-close {  
background: none; border: none;  
color: var(–text2); font-size: 1.5rem;  
cursor: pointer; transition: color 0.2s;  
line-height: 1;  
}  
.cart-close:hover { color: var(–gold2); }  
.cart-items { flex: 1; overflow-y: auto; padding: 20px; }  
.cart-item {  
display: flex;  
gap: 15px;  
padding: 15px 0;  
border-bottom: 1px solid rgba(184,148,63,0.1);  
align-items: center;  
}  
.cart-item-icon { font-size: 2rem; min-width: 50px; text-align: center; }  
.cart-item-info { flex: 1; }  
.cart-item-name { font-size: 0.9rem; color: var(–white); font-weight: 600; }  
.cart-item-price { font-size: 0.85rem; color: var(–gold2); margin-top: 3px; }  
.cart-item-remove {  
background: none; border: none;  
color: var(–text2); cursor: pointer;  
font-size: 1.2rem; transition: color 0.2s;  
}  
.cart-item-remove:hover { color: #e05; }  
.cart-empty {  
text-align: center;  
padding: 60px 20px;  
color: var(–text2);  
}  
.cart-empty-icon { font-size: 4rem; margin-bottom: 15px; opacity: 0.5; }  
.cart-footer {  
padding: 20px 25px;  
border-top: 1px solid rgba(184,148,63,0.15);  
}  
.cart-total {  
display: flex;  
justify-content: space-between;  
align-items: center;  
margin-bottom: 15px;  
font-size: 1rem;  
}  
.cart-total-label { color: var(–text2); letter-spacing: 1px; }  
.cart-total-amount {  
font-family: ‘Playfair Display’, serif;  
font-size: 1.5rem;  
color: var(–gold2);  
}  
.btn-checkout {  
width: 100%;  
background: linear-gradient(135deg, var(–gold), var(–gold2));  
border: none;  
color: var(–dark);  
padding: 14px;  
font-family: ‘Cairo’, sans-serif;  
font-size: 0.9rem;  
font-weight: 700;  
letter-spacing: 2px;  
cursor: pointer;  
text-transform: uppercase;  
transition: all 0.3s;  
}  
.btn-checkout:hover { box-shadow: 0 8px 25px rgba(184,148,63,0.4); }  
.cart-overlay {  
position: fixed; inset: 0;  
background: rgba(0,0,0,0.6);  
z-index: 599;  
opacity: 0;  
visibility: hidden;  
transition: all 0.3s;  
}  
.cart-overlay.open { opacity: 1; visibility: visible; }  
  
/* Success notification */  
.toast {  
position: fixed;  
bottom: 30px;  
left: 50%;  
transform: translateX(-50%) translateY(100px);  
background: var(–dark3);  
border: 1px solid var(–gold);  
color: var(–gold2);  
padding: 14px 30px;  
font-size: 0.9rem;  
letter-spacing: 1px;  
z-index: 9000;  
transition: transform 0.4s cubic-bezier(0.34,1.56,0.64,1);  
white-space: nowrap;  
}  
.toast.show { transform: translateX(-50%) translateY(0); }  
  
/* Newsletter */  
.newsletter {  
background: linear-gradient(135deg, var(–dark3), var(–dark2));  
text-align: center;  
padding: 80px 5%;  
border-top: 1px solid rgba(184,148,63,0.15);  
border-bottom: 1px solid rgba(184,148,63,0.15);  
}  
.newsletter .section-title { margin: 0 auto 15px; }  
.newsletter .section-desc { margin: 0 auto 30px; text-align: center; }  
.newsletter-form {  
display: flex;  
max-width: 500px;  
margin: 0 auto;  
gap: 0;  
}  
.newsletter-input {  
flex: 1;  
background: var(–dark);  
border: 1px solid rgba(184,148,63,0.3);  
border-left: none;  
color: var(–cream);  
padding: 14px 20px;  
font-family: ‘Cairo’, sans-serif;  
font-size: 0.9rem;  
outline: none;  
direction: rtl;  
}  
.newsletter-input:focus { border-color: var(–gold2); }  
.newsletter-btn {  
background: var(–gold);  
border: 1px solid var(–gold);  
color: var(–dark);  
padding: 14px 30px;  
font-family: ‘Cairo’, sans-serif;  
font-size: 0.85rem;  
font-weight: 700;  
cursor: pointer;  
letter-spacing: 1px;  
transition: all 0.3s;  
white-space: nowrap;  
}  
.newsletter-btn:hover { background: var(–gold2); }  
  
/* Footer */  
footer {  
background: var(–dark);  
padding: 60px 5% 30px;  
border-top: 1px solid rgba(184,148,63,0.1);  
}  
.footer-grid {  
display: grid;  
grid-template-columns: 2fr 1fr 1fr 1fr;  
gap: 50px;  
margin-bottom: 40px;  
}  
.footer-logo {  
font-family: ‘Playfair Display’, serif;  
font-size: 1.8rem;  
color: var(–gold2);  
display: block;  
margin-bottom: 15px;  
}  
.footer-desc {  
font-size: 0.85rem;  
color: var(–text2);  
line-height: 1.8;  
margin-bottom: 25px;  
}  
.social-links { display: flex; gap: 12px; }  
.social-link {  
width: 38px; height: 38px;  
border: 1px solid rgba(184,148,63,0.3);  
display: flex; align-items: center; justify-content: center;  
color: var(–text2);  
text-decoration: none;  
font-size: 0.9rem;  
transition: all 0.3s;  
}  
.social-link:hover { border-color: var(–gold); color: var(–gold2); background: rgba(184,148,63,0.1); }  
.footer-heading {  
font-size: 0.75rem;  
letter-spacing: 4px;  
color: var(–gold);  
text-transform: uppercase;  
margin-bottom: 20px;  
}  
.footer-links { list-style: none; }  
.footer-links li { margin-bottom: 10px; }  
.footer-links a {  
color: var(–text2);  
text-decoration: none;  
font-size: 0.85rem;  
transition: color 0.3s;  
letter-spacing: 0.5px;  
}  
.footer-links a:hover { color: var(–gold2); }  
.footer-bottom {  
border-top: 1px solid rgba(184,148,63,0.1);  
padding-top: 25px;  
display: flex;  
justify-content: space-between;  
align-items: center;  
flex-wrap: wrap;  
gap: 15px;  
}  
.footer-copy {  
font-size: 0.75rem;  
color: var(–text2);  
letter-spacing: 1px;  
}  
.footer-copy span { color: var(–gold); }  
  
/* Success modal */  
.success-modal {  
text-align: center;  
padding: 40px;  
}  
.success-icon {  
font-size: 4rem;  
margin-bottom: 20px;  
display: block;  
animation: bounceIn 0.6s cubic-bezier(0.34,1.56,0.64,1);  
}  
@keyframes bounceIn { from{transform:scale(0)} to{transform:scale(1)} }  
.success-title {  
font-family: ‘Playfair Display’, serif;  
font-size: 1.8rem;  
color: var(–gold2);  
margin-bottom: 10px;  
}  
.success-text { color: var(–text2); line-height: 1.8; font-size: 0.95rem; }  
  
/* Scrollbar */  
::-webkit-scrollbar { width: 4px; }  
::-webkit-scrollbar-track { background: var(–dark); }  
::-webkit-scrollbar-thumb { background: var(–gold); }  
  
/* Responsive */  
@media (max-width: 900px) {  
.about-section { grid-template-columns: 1fr; }  
.about-visual { height: 300px; }  
.testimonials-grid { grid-template-columns: 1fr; }  
.footer-grid { grid-template-columns: 1fr 1fr; }  
.features-grid { grid-template-columns: 1fr 1fr; }  
nav .nav-links { display: none; }  
.nav-menu-btn { display: block; }  
}  
@media (max-width: 600px) {  
.products-grid { grid-template-columns: 1fr; }  
.footer-grid { grid-template-columns: 1fr; }  
.features-grid { grid-template-columns: 1fr 1fr; }  
.about-stats { grid-template-columns: 1fr 1fr; }  
.form-row { grid-template-columns: 1fr; }  
.cart-drawer { width: 100vw; }  
.hero-watch-img { display: none; }  
nav { padding: 0 4%; }  
}  
  
/* Fade-in animation on scroll */  
.fade-in {  
opacity: 0;  
transform: translateY(30px);  
transition: opacity 0.7s ease, transform 0.7s ease;  
}  
.fade-in.visible {  
opacity: 1;  
transform: translateY(0);  
}  
</style>  
  
</head>  
<body>  
  
<!-- Cursor -->  
  
<div class="cursor" id="cursor"></div>  
<div class="cursor-ring" id="cursorRing"></div>  
  
<!-- Loader -->  
  
<div id="loader">  
  <div class="loader-logo">Tempo D'or</div>  
  <div class="loader-bar"><div class="loader-fill"></div></div>  
</div>  
  
<!-- Navigation -->  
  
<nav id="navbar">  
  <a href="#" class="nav-logo">Tempo <span>D'or</span></a>  
  <ul class="nav-links">  
    <li><a href="#products">المنتجات</a></li>  
    <li><a href="#about">عن المتجر</a></li>  
    <li><a href="#testimonials">آراء العملاء</a></li>  
    <li><a href="#contact">تواصل معنا</a></li>  
  </ul>  
  <button class="nav-cart" onclick="toggleCart()">  
    <span>🛒</span>  
    <span>السلة</span>  
    <span class="cart-count" id="cartCount">0</span>  
  </button>  
  <button class="nav-menu-btn" id="menuBtn">☰</button>  
</nav>  
  
<!-- Hero -->  
  
<section class="hero">  
  <div class="hero-bg-pattern"></div>  
  <div class="hero-lines"></div>  
  <div class="hero-content">  
    <p class="hero-eyebrow">وقت من ذهب</p>  
    <h1 class="hero-title">  
      الفخامة في<br>  
      <em>كل لحظة</em>  
    </h1>  
    <p class="hero-subtitle">ساعات فاخرة تعكس شخصيتك</p>  
    <a href="#products" class="hero-cta">  
      <span>اكتشف المجموعة</span>  
      <span>←</span>  
    </a>  
  </div>  
  <div class="hero-scroll">مرر للأسفل</div>  
</section>  
  
<!-- Features -->  
  
<div class="features fade-in">  
  <div class="features-grid">  
    <div class="feature-item">  
      <span class="feature-icon">🚚</span>  
      <div class="feature-title">توصيل مجاني</div>  
      <div class="feature-desc">لجميع الطلبات فوق 500 ريال</div>  
    </div>  
    <div class="feature-item">  
      <span class="feature-icon">✅</span>  
      <div class="feature-title">ضمان الأصالة</div>  
      <div class="feature-desc">جميع ساعاتنا أصلية 100%</div>  
    </div>  
    <div class="feature-item">  
      <span class="feature-icon">🔄</span>  
      <div class="feature-title">إرجاع مجاني</div>  
      <div class="feature-desc">خلال 30 يوم من الشراء</div>  
    </div>  
    <div class="feature-item">  
      <span class="feature-icon">💎</span>  
      <div class="feature-title">خدمة VIP</div>  
      <div class="feature-desc">دعم مخصص على مدار الساعة</div>  
    </div>  
  </div>  
</div>  
  
<!-- Products -->  
  
<section class="products-section" id="products">  
  <div class="products-header fade-in">  
    <div>  
      <p class="section-label">تشكيلتنا</p>  
      <h2 class="section-title">ساعات <em>مختارة</em></h2>  
      <div class="gold-line"></div>  
    </div>  
    <div class="filter-tabs">  
      <button class="filter-tab active" onclick="filterProducts('all', this)">الكل</button>  
      <button class="filter-tab" onclick="filterProducts('classic', this)">كلاسيك</button>  
      <button class="filter-tab" onclick="filterProducts('sport', this)">رياضية</button>  
      <button class="filter-tab" onclick="filterProducts('luxury', this)">فاخرة</button>  
    </div>  
  </div>  
  <div class="products-grid" id="productsGrid"></div>  
</section>  
  
<!-- About -->  
  
<section class="about-section fade-in" id="about">  
  <div class="about-visual">  
    <div class="about-circle"></div>  
    <div class="about-circle"></div>  
    <div class="about-circle"></div>  
    <div class="about-center">⌚</div>  
  </div>  
  <div>  
    <p class="section-label">من نحن</p>  
    <h2 class="section-title">قصة <em>Tempo D'or</em></h2>  
    <div class="gold-line"></div>  
    <p class="section-desc">منذ تأسيسنا، نحن نؤمن بأن الساعة الجيدة ليست مجرد أداة لقياس الوقت، بل هي تعبير عن الذوق الرفيع والشخصية المميزة. نقدم لك أفضل الماركات العالمية بأسعار تنافسية.</p>  
    <div class="about-stats">  
      <div class="stat-box fade-in">  
        <span class="stat-number">+500</span>  
        <span class="stat-label">طراز متاح</span>  
      </div>  
      <div class="stat-box fade-in">  
        <span class="stat-number">+10k</span>  
        <span class="stat-label">عميل سعيد</span>  
      </div>  
      <div class="stat-box fade-in">  
        <span class="stat-number">5★</span>  
        <span class="stat-label">تقييم العملاء</span>  
      </div>  
      <div class="stat-box fade-in">  
        <span class="stat-number">7</span>  
        <span class="stat-label">سنوات خبرة</span>  
      </div>  
    </div>  
  </div>  
</section>  
  
<!-- Testimonials -->  
  
<section class="testimonials fade-in" id="testimonials">  
  <div style="text-align:center; max-width:600px; margin:0 auto 50px;">  
    <p class="section-label">آراء عملائنا</p>  
    <h2 class="section-title">ماذا يقولون عنّا</h2>  
    <div class="gold-line" style="margin:20px auto;"></div>  
  </div>  
  <div class="testimonials-grid">  
    <div class="testimonial-card fade-in">  
      <div class="stars">★★★★★</div>  
      <p class="testimonial-text">"وصلتني الساعة في أقل من يومين، والجودة فاقت توقعاتي تماماً. سأكون عميلاً دائماً لمتجر Tempo D'or بكل تأكيد."</p>  
      <div class="testimonial-author">  
        <div class="author-avatar">👨</div>  
        <div>  
          <div class="author-name">محمد العنزي</div>  
          <div class="author-loc">الرياض، السعودية</div>  
        </div>  
      </div>  
    </div>  
    <div class="testimonial-card fade-in">  
      <div class="stars">★★★★★</div>  
      <p class="testimonial-text">"اشتريت ساعة هدية لزوجي وكان مبهوتاً من الشكل والتغليف الراقي. خدمة العملاء ممتازة وردوا على كل استفساراتي."</p>  
      <div class="testimonial-author">  
        <div class="author-avatar">👩</div>  
        <div>  
          <div class="author-name">سارة الخالدي</div>  
          <div class="author-loc">دبي، الإمارات</div>  
        </div>  
      </div>  
    </div>  
    <div class="testimonial-card fade-in">  
      <div class="stars">★★★★★</div>  
      <p class="testimonial-text">"أفضل متجر ساعات أون لاين تعاملت معه. الأسعار عادلة والمنتجات أصلية ١٠٠٪. شكراً على الخدمة الرائعة."</p>  
      <div class="testimonial-author">  
        <div class="author-avatar">👨‍💼</div>  
        <div>  
          <div class="author-name">خالد السلمي</div>  
          <div class="author-loc">الكويت</div>  
        </div>  
      </div>  
    </div>  
  </div>  
</section>  
  
<!-- Newsletter -->  
  
<div class="newsletter fade-in">  
  <p class="section-label" style="text-align:center">نشرتنا البريدية</p>  
  <h2 class="section-title">كن أول من يعلم</h2>  
  <p class="section-desc" style="text-align:center">اشترك واحصل على خصم 10% على أول طلب</p>  
  <div class="newsletter-form">  
    <input type="email" class="newsletter-input" placeholder="بريدك الإلكتروني...">  
    <button class="newsletter-btn" onclick="subscribeNewsletter()">اشترك الآن</button>  
  </div>  
</div>  
  
<!-- Footer -->  
  
<footer id="contact">  
  <div class="footer-grid">  
    <div>  
      <a href="#" class="footer-logo">Tempo D'or</a>  
      <p class="footer-desc">وقت من ذهب — نقدم لك أفخر الساعات العالمية بأسعار استثنائية، مع ضمان الجودة والأصالة في كل قطعة.</p>  
      <div class="social-links">  
        <a class="social-link" href="#" title="Instagram">📸</a>  
        <a class="social-link" href="#" title="Twitter">🐦</a>  
        <a class="social-link" href="#" title="WhatsApp">💬</a>  
        <a class="social-link" href="#" title="TikTok">🎵</a>  
      </div>  
    </div>  
    <div>  
      <h4 class="footer-heading">روابط سريعة</h4>  
      <ul class="footer-links">  
        <li><a href="#products">المنتجات</a></li>  
        <li><a href="#about">عن المتجر</a></li>  
        <li><a href="#testimonials">آراء العملاء</a></li>  
        <li><a href="#">سياسة الخصوصية</a></li>  
      </ul>  
    </div>  
    <div>  
      <h4 class="footer-heading">خدمة العملاء</h4>  
      <ul class="footer-links">  
        <li><a href="#">تتبع طلبك</a></li>  
        <li><a href="#">سياسة الإرجاع</a></li>  
        <li><a href="#">دليل المقاسات</a></li>  
        <li><a href="#">الأسئلة الشائعة</a></li>  
      </ul>  
    </div>  
    <div>  
      <h4 class="footer-heading">تواصل معنا</h4>  
      <ul class="footer-links">  
        <li><a href="tel:+966500000000">📞 +966 50 000 0000</a></li>  
        <li><a href="mailto:info@tempodor.com">✉️ info@tempodor.com</a></li>  
        <li><a href="#">💬 واتساب</a></li>  
        <li><a href="#">📍 عنوان المتجر</a></li>  
      </ul>  
    </div>  
  </div>  
  <div class="footer-bottom">  
    <p class="footer-copy">© 2025 <span>Tempo D'or</span> — جميع الحقوق محفوظة</p>  
    <p class="footer-copy">صُنع بـ ❤️ للفخامة العربية</p>  
  </div>  
</footer>  
  
<!-- Cart Drawer -->  
  
<div class="cart-overlay" id="cartOverlay" onclick="toggleCart()"></div>  
<div class="cart-drawer" id="cartDrawer">  
  <div class="cart-drawer-header">  
    <span class="cart-drawer-title">سلة المشتريات</span>  
    <button class="cart-close" onclick="toggleCart()">×</button>  
  </div>  
  <div class="cart-items" id="cartItems">  
    <div class="cart-empty" id="cartEmpty">  
      <div class="cart-empty-icon">🛒</div>  
      <p style="color:var(--text2)">سلتك فارغة حتى الآن</p>  
    </div>  
  </div>  
  <div class="cart-footer">  
    <div class="cart-total">  
      <span class="cart-total-label">الإجمالي</span>  
      <span class="cart-total-amount" id="cartTotal">0 ر.س</span>  
    </div>  
    <button class="btn-checkout" onclick="checkoutCart()">إتمام الطلب ←</button>  
  </div>  
</div>  
  
<!-- Order Modal -->  
  
<div class="modal-overlay" id="orderModal">  
  <div class="modal">  
    <div class="modal-header">  
      <span class="modal-title">إتمام الطلب</span>  
      <button class="modal-close" onclick="closeModal()">×</button>  
    </div>  
    <div class="modal-body" id="modalBody">  
      <!-- filled by JS -->  
    </div>  
  </div>  
</div>  
  
<!-- Toast -->  
  
<div class="toast" id="toast"></div>  
  
<script>  
// --- Cursor ---  
const cursor = document.getElementById('cursor');  
const ring = document.getElementById('cursorRing');  
let mx=0,my=0,rx=0,ry=0;  
document.addEventListener('mousemove', e => { mx=e.clientX; my=e.clientY; cursor.style.left=mx-6+'px'; cursor.style.top=my-6+'px'; });  
(function animRing(){ rx+=(mx-rx)*0.12; ry+=(my-ry)*0.12; ring.style.left=rx-18+'px'; ring.style.top=ry-18+'px'; requestAnimationFrame(animRing); })();  
  
// --- Loader ---  
setTimeout(() => document.getElementById('loader').classList.add('hide'), 2200);  
  
// --- Navbar scroll ---  
window.addEventListener('scroll', () => {  
  document.getElementById('navbar').classList.toggle('scrolled', window.scrollY > 60);  
});  
  
// --- Fade-in on scroll ---  
const observer = new IntersectionObserver(entries => {  
  entries.forEach(e => { if(e.isIntersecting) e.target.classList.add('visible'); });  
}, { threshold: 0.12 });  
document.querySelectorAll('.fade-in').forEach(el => observer.observe(el));  
  
// --- Products Data ---  
const products = [  
  { id:1, name:"Chrono Élite", category:"luxury", price:2800, oldPrice:3500, desc:"ساعة فاخرة بهيكل من الفولاذ المصقول مع حركة سويسرية دقيقة", badge:"الأكثر مبيعاً", color:"#B8943F", emoji:"⌚" },  
  { id:2, name:"Sport Master X", category:"sport", price:950, oldPrice:1200, desc:"مقاومة للماء حتى 200م، مثالية لكل مغامرة رياضية", badge:"جديد", color:"#2A5F8F", emoji:"🏅" },  
  { id:3, name:"Heritage Classic", category:"classic", price:1650, oldPrice:null, desc:"تصميم كلاسيكي خالد مستوحى من الساعات الأوروبية العريقة", badge:null, color:"#4A3520", emoji:"🕰️" },  
  { id:4, name:"Rose Gold Lady", category:"luxury", price:2200, oldPrice:2900, desc:"ساعة نسائية أنيقة بالذهب الوردي وإبزيم الألماس", badge:"حصري", color:"#C06080", emoji:"💎" },  
  { id:5, name:"Pilot Pro 500", category:"sport", price:1100, oldPrice:1400, desc:"مستوحاة من ساعات الطيارين، بتصميم عسكري أنيق", badge:null, color:"#2A2518", emoji:"✈️" },  
  { id:6, name:"Vintage Royale", category:"classic", price:3200, oldPrice:null, desc:"قطعة فنية نادرة بالذهب الأصفر عيار 18، مرجع الأناقة", badge:"محدود", color:"#8B6914", emoji:"👑" },  
];  
  
let cart = [];  
let currentFilter = 'all';  
  
function renderProducts(filter = 'all') {  
  const grid = document.getElementById('productsGrid');  
  const filtered = filter === 'all' ? products : products.filter(p => p.category === filter);  
  grid.innerHTML = filtered.map(p => `  
    <div class="product-card fade-in" data-id="${p.id}">  
      ${p.badge ? `<div class="product-badge ${p.badge==='جديد'?'new':''}">${p.badge}</div>` : ''}  
      <div class="product-img-wrap">  
        <div class="watch-visual" style="border-color:${p.color}; color:${p.color}">  
          ${p.emoji}  
        </div>  
      </div>  
      <div class="product-info">  
        <div class="product-category">${{luxury:'فاخرة',sport:'رياضية',classic:'كلاسيك'}[p.category]}</div>  
        <div class="product-name">${p.name}</div>  
        <div class="product-desc">${p.desc}</div>  
        <div class="product-footer">  
          <div class="product-price">  
            ${p.oldPrice ? `<span class="price-old">${p.oldPrice.toLocaleString()} <span class="price-currency">ر.س</span></span>` : ''}  
            <span class="price-new">${p.price.toLocaleString()} <span class="price-currency">ر.س</span></span>  
          </div>  
          <button class="btn-add-cart" onclick="addToCart(${p.id})">  
            <span>+</span> أضف للسلة  
          </button>  
        </div>  
      </div>  
    </div>  
  `).join('');  
  // Re-observe new cards  
  grid.querySelectorAll('.fade-in').forEach(el => observer.observe(el));  
}  
  
function filterProducts(cat, btn) {  
  document.querySelectorAll('.filter-tab').forEach(b => b.classList.remove('active'));  
  btn.classList.add('active');  
  renderProducts(cat);  
}  
  
// --- Cart ---  
function addToCart(id) {  
  const p = products.find(x => x.id === id);  
  const existing = cart.find(x => x.id === id);  
  if (existing) existing.qty++;  
  else cart.push({ ...p, qty: 1 });  
  updateCartUI();  
  showToast(`✅ تم إضافة "${p.name}" للسلة`);  
}  
  
function removeFromCart(id) {  
  cart = cart.filter(x => x.id !== id);  
  updateCartUI();  
}  
  
function updateCartUI() {  
  const count = cart.reduce((s,x) => s+x.qty, 0);  
  document.getElementById('cartCount').textContent = count;  
  const total = cart.reduce((s,x) => s + x.price*x.qty, 0);  
  document.getElementById('cartTotal').textContent = total.toLocaleString() + ' ر.س';  
  const container = document.getElementById('cartItems');  
  const empty = document.getElementById('cartEmpty');  
  if (cart.length === 0) {  
    empty.style.display = 'block';  
    container.querySelectorAll('.cart-item').forEach(e => e.remove());  
  } else {  
    empty.style.display = 'none';  
    const existing = container.querySelectorAll('.cart-item');  
    existing.forEach(e => e.remove());  
    cart.forEach(item => {  
      const div = document.createElement('div');  
      div.className = 'cart-item';  
      div.innerHTML = `  
        <div class="cart-item-icon">${item.emoji}</div>  
        <div class="cart-item-info">  
          <div class="cart-item-name">${item.name} ${item.qty > 1 ? '×'+item.qty : ''}</div>  
          <div class="cart-item-price">${(item.price*item.qty).toLocaleString()} ر.س</div>  
        </div>  
        <button class="cart-item-remove" onclick="removeFromCart(${item.id})">🗑</button>  
      `;  
      container.insertBefore(div, empty);  
    });  
  }  
}  
  
function toggleCart() {  
  document.getElementById('cartDrawer').classList.toggle('open');  
  document.getElementById('cartOverlay').classList.toggle('open');  
}  
  
function checkoutCart() {  
  if (cart.length === 0) { showToast('⚠️ أضف منتجاً أولاً'); return; }  
  toggleCart();  
  openCheckoutModal();  
}  
  
// --- Order Modal ---  
let selectedProduct = null;  
  
function openCheckoutModal() {  
  const total = cart.reduce((s,x)=>s+x.price*x.qty,0);  
  const itemsHtml = cart.map(i=>`<div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:10px;"><span style="color:var(--cream2);font-size:.85rem">${i.emoji} ${i.name} ×${i.qty}</span><span style="color:var(--gold2);font-weight:600">${(i.price*i.qty).toLocaleString()} ر.س</span></div>`).join('');  
  document.getElementById('modalBody').innerHTML = `  
    <div style="background:var(--dark3);border:1px solid rgba(184,148,63,.15);padding:20px;margin-bottom:25px;">  
      ${itemsHtml}  
      <div style="border-top:1px solid rgba(184,148,63,.2);margin-top:10px;padding-top:10px;display:flex;justify-content:space-between;">  
        <span style="color:var(--gold);letter-spacing:1px;font-size:.85rem">TOTAL</span>  
        <span style="color:var(--gold2);font-size:1.2rem;font-weight:700">${total.toLocaleString()} ر.س</span>  
      </div>  
    </div>  
    <div class="form-group">  
      <label class="form-label">الاسم الكامل</label>  
      <input type="text" class="form-input" id="oName" placeholder="أدخل اسمك الكامل">  
    </div>  
    <div class="form-row">  
      <div class="form-group">  
        <label class="form-label">رقم الجوال</label>  
        <input type="tel" class="form-input" id="oPhone" placeholder="05xxxxxxxx">  
      </div>  
      <div class="form-group">  
        <label class="form-label">المدينة</label>  
        <select class="form-select" id="oCity">  
          <option>اختر المدينة</option>  
          <option>الرياض</option><option>جدة</option><option>الدمام</option>  
          <option>مكة المكرمة</option><option>المدينة المنورة</option>  
          <option>الكويت</option><option>دبي</option><option>أبوظبي</option>  
          <option>عمّان</option><option>بيروت</option><option>القاهرة</option>  
          <option>أخرى</option>  
        </select>  
      </div>  
    </div>  
    <div class="form-group">  
      <label class="form-label">العنوان التفصيلي</label>  
      <textarea class="form-textarea" id="oAddress" placeholder="الحي، الشارع، رقم المبنى..."></textarea>  
  
```  
</div>  
<div class="form-group">  
  <label class="form-label">طريقة الدفع</label>  
  <select class="form-select" id="oPayment">  
    <option>الدفع عند الاستلام</option>  
    <option>تحويل بنكي</option>  
    <option>مدى / فيزا</option>  
  </select>  
</div>  
<button class="btn-submit" onclick="submitOrder()">✅ تأكيد الطلب الآن</button>  
```  
  
`;  
document.getElementById(‘orderModal’).classList.add(‘open’);  
}  
  
function closeModal() { document.getElementById(‘orderModal’).classList.remove(‘open’); }  
  
function submitOrder() {  
const name = document.getElementById(‘oName’)?.value;  
const phone = document.getElementById(‘oPhone’)?.value;  
const city = document.getElementById(‘oCity’)?.value;  
const address = document.getElementById(‘oAddress’)?.value;  
if (!name||!phone||city===‘اختر المدينة’||!address) {  
showToast(‘⚠️ يرجى ملء جميع الحقول’); return;  
}  
document.getElementById(‘modalBody’).innerHTML = `<div class="success-modal"> <span class="success-icon">🎉</span> <h3 class="success-title">تم تأكيد طلبك!</h3> <p class="success-text">شكراً لك <strong style="color:var(--gold2)">${name}</strong>!<br> سيتواصل معك فريقنا خلال 24 ساعة على الرقم<br> <strong style="color:var(--gold2)">${phone}</strong><br>لتأكيد التوصيل إلى ${city}.</p> <button class="btn-submit" style="margin-top:25px" onclick="closeModal();resetCart()">العودة للتسوق</button> </div>`;  
cart = [];  
updateCartUI();  
}  
  
function resetCart() { cart = []; updateCartUI(); }  
  
// — Toast —  
function showToast(msg) {  
const t = document.getElementById(‘toast’);  
t.textContent = msg;  
t.classList.add(‘show’);  
setTimeout(() => t.classList.remove(‘show’), 3000);  
}  
  
// — Newsletter —  
function subscribeNewsletter() {  
const inp = document.querySelector(’.newsletter-input’);  
if (!inp.value || !inp.value.includes(’@’)) { showToast(‘⚠️ أدخل بريداً إلكترونياً صحيحاً’); return; }  
showToast(‘🎁 تم الاشتراك! ستصلك كوبون الخصم قريباً’);  
inp.value = ‘’;  
}  
  
// — Init —  
renderProducts();  
</script>  
  
</body>  
</html>  
