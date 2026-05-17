<!DOCTYPE html>  
  
<html lang="ar" dir="rtl">  
<head>  
<meta charset="UTF-8">  
<meta name="viewport" content="width=device-width, initial-scale=1.0">  
<title>Tempo D'or | For Watches</title>  
  
<style>  
*,*::before,*::after{margin:0;padding:0;box-sizing:border-box;}  
a{color:inherit;text-decoration:none;}  
  
:root{  
  --gold:#8B6914;  
  --gold2:#A07820;  
  --gold3:#C9A84C;  
  --gold4:#E8C96A;  
  --white:#FFFFFF;  
  --off:#FAF8F3;  
  --dark:#1A1600;  
  --text:#1A1600;  
  --text2:#5A4A20;  
  --red:#E03030;  
  --fn:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;  
}  
  
html{scroll-behavior:smooth;}  
body{font-family:'SF Arabic','Geeza Pro','Cairo',Tahoma,Arial,sans-serif;background:#fff;color:var(--text);overflow-x:hidden;}  
::-webkit-scrollbar{width:4px;}  
::-webkit-scrollbar-thumb{background:var(--gold2);}  
  
/* ===== NAV ===== */  
nav{  
  position:fixed;top:0;left:0;right:0;z-index:200;  
  background:#fff;  
  border-bottom:2px solid var(--gold);  
  padding:0 5%;height:70px;  
  display:flex;align-items:center;justify-content:space-between;  
  box-shadow:0 2px 15px rgba(139,105,20,0.15);  
  transition:height 0.3s;  
}  
nav.scrolled{height:58px;}  
.nav-logo img{height:50px;object-fit:contain;}  
nav.scrolled .nav-logo img{height:40px;}  
.nav-links{display:flex;gap:25px;list-style:none;}  
.nav-links a{color:var(--text2);font-size:0.85rem;font-weight:600;font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;transition:color 0.3s;}  
.nav-links a:hover{color:var(--gold);}  
.nav-right{display:flex;align-items:center;gap:12px;}  
.nav-cart-btn{  
  background:var(--gold) !important;  
  border:none;  
  color:#fff !important;  
  padding:9px 18px;  
  font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;  
  font-size:0.82rem;font-weight:700;  
  cursor:pointer;border-radius:4px;  
  display:flex;align-items:center;gap:7px;  
  box-shadow:0 3px 10px rgba(139,105,20,0.35);  
  transition:all 0.3s;  
}  
.nav-cart-btn:hover{background:var(--gold2) !important;transform:translateY(-1px);}  
.nav-cart-btn span{color:#fff !important;}  
.cart-count{  
  background:var(--red);color:#fff !important;  
  border-radius:50%;width:20px;height:20px;  
  font-size:0.7rem;font-weight:900;  
  display:flex;align-items:center;justify-content:center;  
}  
.nav-menu-btn{display:none;background:none;border:none;font-size:1.5rem;color:var(--gold);cursor:pointer;}  
  
/* ===== HERO ===== */  
.hero{  
  min-height:100vh;  
  background:linear-gradient(135deg,#F5EDD5,#EDE0C0,#E8D5B0);  
  display:flex;align-items:center;  
  padding:90px 5% 60px;  
  position:relative;overflow:hidden;  
}  
.hero-grid{  
  display:grid;grid-template-columns:1fr 1fr;  
  gap:50px;align-items:center;  
  max-width:1200px;margin:0 auto;width:100%;  
}  
.hero-text{animation:fadeUp 0.8s ease both;}  
@keyframes fadeUp{from{opacity:0;transform:translateY(30px)}to{opacity:1;transform:translateY(0)}}  
.hero-eyebrow{font-size:0.7rem;letter-spacing:4px;color:var(--dark);text-transform:uppercase;margin-bottom:14px;font-weight:600;font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;}  
.hero-title{font-size:clamp(2.2rem,5vw,3.8rem);font-weight:900;color:var(--dark);margin-bottom:18px;line-height:1.2;font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;}  
.hero-title span{color:var(--gold2);}  
.hero-sub{font-size:0.95rem;color:var(--text2);line-height:1.8;margin-bottom:30px;font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;}  
.hero-btn{  
  display:inline-flex;align-items:center;gap:10px;  
  background:linear-gradient(135deg,var(--gold),var(--gold3));  
  color:#fff !important;padding:13px 32px;  
  font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;font-size:0.9rem;font-weight:700;  
  border:none;cursor:pointer;border-radius:4px;  
  box-shadow:0 6px 20px rgba(139,105,20,0.35);  
  transition:all 0.3s;  
}  
.hero-btn:hover{transform:translateY(-2px);box-shadow:0 10px 28px rgba(139,105,20,0.45);}  
.hero-img-wrap{animation:fadeUp 0.8s ease 0.2s both;}  
.hero-img-wrap img{width:100%;max-width:480px;background:transparent;}  
  
/* ===== FEATURES ===== */  
.features-bar{  
  background:var(--gold);  
  padding:16px 5%;  
  display:flex;justify-content:center;gap:40px;flex-wrap:wrap;  
}  
.feat-item{display:flex;align-items:center;gap:8px;color:#fff;font-size:0.82rem;font-weight:600;font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;}  
  
/* ===== SECTION COMMON ===== */  
.section{padding:75px 5%;}  
.section.bg-off{background:var(--off);}  
.section.bg-white{background:#fff;}  
.sec-head{text-align:center;margin-bottom:45px;}  
.sec-label{font-size:0.7rem;letter-spacing:3px;color:var(--gold);text-transform:uppercase;margin-bottom:8px;font-weight:700;font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;}  
.sec-title{font-size:clamp(1.7rem,3.5vw,2.6rem);font-weight:900;color:var(--dark);margin-bottom:10px;font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;}  
.sec-title span{color:var(--gold2);}  
.sec-line{width:55px;height:3px;background:linear-gradient(to left,var(--gold),var(--gold4));margin:0 auto;border-radius:3px;}  
  
/* ===== FILTER ===== */  
.filter-wrap{display:flex;justify-content:center;gap:8px;margin-bottom:35px;flex-wrap:wrap;}  
.filter-btn{  
  padding:8px 20px;  
  background:#fff;  
  border:2px solid var(--gold);  
  color:var(--gold);  
  font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;font-size:0.8rem;font-weight:700;  
  cursor:pointer;border-radius:50px;  
  transition:all 0.25s;  
}  
.filter-btn:hover,.filter-btn.active{  
  background:var(--gold);  
  color:#fff;  
  box-shadow:0 4px 12px rgba(139,105,20,0.3);  
}  
  
/* ===== PRODUCTS ===== */  
.products-grid{  
  display:grid;  
  grid-template-columns:repeat(auto-fill,minmax(260px,1fr));  
  gap:22px;max-width:1200px;margin:0 auto;  
}  
.product-card{  
  background:#fff;border-radius:12px;  
  overflow:hidden;  
  box-shadow:0 3px 18px rgba(0,0,0,0.08);  
  border:1.5px solid rgba(139,105,20,0.12);  
  cursor:pointer;  
  transition:all 0.3s cubic-bezier(0.34,1.56,0.64,1);  
}  
.product-card:hover{  
  transform:translateY(-7px) scale(1.01);  
  box-shadow:0 18px 45px rgba(139,105,20,0.18);  
  border-color:var(--gold);  
}  
.card-badge{  
  position:absolute;top:13px;right:13px;z-index:3;  
  padding:4px 11px;border-radius:50px;  
  font-size:0.68rem;font-weight:700;font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;  
}  
.badge-sold,.badge-sale{background:rgba(224,48,48,0.92);color:#fff;}  
.card-img{height:230px;overflow:hidden;position:relative;background:#f0ead8;}  
.card-img img{width:100%;height:100%;object-fit:cover;transition:transform 0.5s;}  
.product-card:hover .card-img img{transform:scale(1.07);}  
.sold-overlay{  
  position:absolute;inset:0;  
  background:rgba(0,0,0,0.4);  
  display:flex;align-items:center;justify-content:center;  
  color:#fff;font-size:1rem;font-weight:900;font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;  
}  
.color-dots{display:flex;gap:5px;padding:10px 16px 0;justify-content:flex-end;}  
.color-dot{width:13px;height:13px;border-radius:50%;border:2px solid rgba(0,0,0,0.12);cursor:pointer;transition:transform 0.2s;}  
.color-dot:hover{transform:scale(1.4);}  
.card-info{padding:10px 16px 16px;}  
.card-cat{font-size:0.65rem;letter-spacing:2px;color:var(--gold);text-transform:uppercase;margin-bottom:3px;font-weight:700;font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;text-align:right;}  
.card-name{font-size:0.98rem;font-weight:700;color:var(--dark);margin-bottom:7px;text-align:right;font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;}  
.card-price{display:flex;align-items:center;gap:8px;margin-bottom:12px;justify-content:flex-end;flex-wrap:wrap;}  
.price-old{font-size:0.85rem;color:var(--red);text-decoration:line-through;font-weight:700;font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;}  
.price-new{font-size:1.1rem;font-weight:900;color:var(--gold2);font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;}  
.price-sold{font-size:0.9rem;font-weight:900;color:var(--red);font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;}  
.price-sale{font-size:1.1rem;font-weight:900;color:var(--red);font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;}  
.card-actions{display:flex;gap:7px;}  
.btn-order{  
  flex:1;  
  background:linear-gradient(135deg,var(--gold),var(--gold3));  
  border:none;color:#fff;padding:9px;  
  font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;font-size:0.8rem;font-weight:700;  
  cursor:pointer;border-radius:6px;  
  box-shadow:0 3px 10px rgba(139,105,20,0.28);  
  transition:all 0.3s;  
}  
.btn-order:hover{transform:translateY(-1px);box-shadow:0 6px 16px rgba(139,105,20,0.38);}  
.btn-order:disabled{background:#bbb;color:#888;cursor:not-allowed;box-shadow:none;transform:none;}  
.btn-cart{  
  background:none;border:2px solid var(--gold);  
  color:var(--gold);padding:9px 13px;  
  font-size:1rem;font-weight:700;  
  cursor:pointer;border-radius:6px;  
  transition:all 0.3s;  
}  
.btn-cart:hover{background:var(--gold);color:#fff;}  
.btn-cart:disabled{opacity:0.4;cursor:not-allowed;}  
  
/* ===== MODAL ===== */  
.modal-overlay{  
  position:fixed;inset:0;z-index:500;  
  background:rgba(0,0,0,0.65);backdrop-filter:blur(5px);  
  display:flex;align-items:center;justify-content:center;  
  padding:20px;opacity:0;visibility:hidden;transition:all 0.3s;  
}  
.modal-overlay.open{opacity:1;visibility:visible;}  
.product-modal{  
  background:#fff;border-radius:14px;  
  max-width:800px;width:100%;max-height:90vh;overflow-y:auto;  
  transform:scale(0.9) translateY(20px);  
  transition:transform 0.3s cubic-bezier(0.34,1.56,0.64,1);  
  border:1px solid rgba(139,105,20,0.2);  
}  
.modal-overlay.open .product-modal{transform:scale(1) translateY(0);}  
.modal-header{  
  display:flex;justify-content:space-between;align-items:center;  
  padding:16px 22px;border-bottom:1px solid rgba(139,105,20,0.15);  
  position:sticky;top:0;background:#fff;z-index:10;border-radius:14px 14px 0 0;  
}  
.modal-title{font-size:1.05rem;font-weight:700;color:var(--gold);font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;}  
.modal-close{background:none;border:none;font-size:1.4rem;cursor:pointer;color:var(--text2);line-height:1;}  
.modal-close:hover{color:var(--red);}  
.modal-body{display:grid;grid-template-columns:1fr 1fr;}  
.modal-img{background:#f0ead8;min-height:300px;overflow:hidden;}  
.modal-img img{width:100%;height:100%;object-fit:cover;transition:opacity 0.3s;}  
.modal-info{padding:25px 22px;background:#fff;}  
.modal-cat{font-size:0.65rem;letter-spacing:2px;color:var(--gold);text-transform:uppercase;margin-bottom:5px;font-weight:700;font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;}  
.modal-name{font-size:1.3rem;font-weight:900;color:var(--dark);margin-bottom:5px;font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;}  
.modal-desc{font-size:0.82rem;color:var(--text2);line-height:1.7;margin-bottom:12px;font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;}  
.modal-prices{display:flex;align-items:center;gap:10px;margin-bottom:16px;flex-wrap:wrap;}  
.modal-p-old{font-size:0.95rem;color:var(--red);text-decoration:line-through;font-weight:700;}  
.modal-p-new{font-size:1.7rem;font-weight:900;color:var(--gold2);}  
.modal-p-sale{font-size:1.7rem;font-weight:900;color:var(--red);}  
.modal-p-sold{font-size:0.95rem;font-weight:700;color:var(--red);}  
.color-sec{margin-bottom:15px;}  
.color-lbl{font-size:0.7rem;letter-spacing:2px;color:var(--text2);text-transform:uppercase;margin-bottom:8px;font-weight:600;font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;}  
.color-opts{display:flex;gap:6px;flex-wrap:wrap;}  
.color-opt{  
  padding:5px 13px;border:2px solid rgba(139,105,20,0.3);  
  background:#fff;font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;font-size:0.78rem;font-weight:600;  
  cursor:pointer;border-radius:50px;color:var(--text2);transition:all 0.2s;  
}  
.color-opt.active,.color-opt:hover{border-color:var(--gold);background:var(--gold);color:#fff;}  
.form-row{display:grid;grid-template-columns:1fr 1fr;gap:9px;margin-bottom:9px;}  
.form-g{margin-bottom:9px;}  
.form-lbl{display:block;font-size:0.68rem;letter-spacing:2px;color:var(--gold);text-transform:uppercase;margin-bottom:4px;font-weight:700;font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;}  
.form-in,.form-sel{  
  width:100%;background:var(--off);  
  border:1.5px solid rgba(139,105,20,0.2);  
  color:var(--dark);padding:9px 12px;  
  font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;font-size:0.86rem;  
  border-radius:6px;outline:none;direction:rtl;  
  transition:border-color 0.3s;  
}  
.form-in:focus,.form-sel:focus{border-color:var(--gold2);background:#fff;}  
.btn-submit{  
  width:100%;  
  background:linear-gradient(135deg,var(--gold),var(--gold3));  
  border:none;color:#fff;padding:12px;  
  font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;font-size:0.9rem;font-weight:700;  
  cursor:pointer;border-radius:8px;  
  box-shadow:0 5px 18px rgba(139,105,20,0.38);  
  transition:all 0.3s;margin-top:8px;  
  display:flex;align-items:center;justify-content:center;gap:8px;  
}  
.btn-submit:hover{transform:translateY(-2px);box-shadow:0 9px 25px rgba(139,105,20,0.48);}  
.sold-msg{text-align:center;padding:22px 0;color:var(--red);font-weight:700;font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;}  
  
/* ===== CART ===== */  
.cart-bg{position:fixed;inset:0;background:rgba(0,0,0,0.5);z-index:599;opacity:0;visibility:hidden;transition:all 0.3s;}  
.cart-bg.open{opacity:1;visibility:visible;}  
.cart-drawer{  
  position:fixed;top:0;left:0;width:380px;max-width:100vw;height:100vh;  
  background:#fff;border-right:2px solid var(--gold);  
  z-index:600;transform:translateX(-100%);  
  transition:transform 0.4s cubic-bezier(0.4,0,0.2,1);  
  display:flex;flex-direction:column;  
}  
.cart-drawer.open{transform:translateX(0);}  
.cart-head{  
  padding:18px 20px;border-bottom:1px solid rgba(139,105,20,0.15);  
  display:flex;align-items:center;justify-content:space-between;  
  background:var(--off);  
}  
.cart-ttl{font-size:1rem;font-weight:700;color:var(--gold);font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;}  
.cart-cls{background:none;border:none;font-size:1.3rem;cursor:pointer;color:var(--text2);}  
.cart-cls:hover{color:var(--red);}  
.cart-items{flex:1;overflow-y:auto;padding:12px;}  
.cart-item{  
  display:flex;gap:10px;padding:11px;  
  background:var(--off);border-radius:8px;  
  margin-bottom:9px;border:1px solid rgba(139,105,20,0.1);  
}  
.cart-item-img{width:55px;height:55px;border-radius:6px;object-fit:cover;}  
.cart-item-info{flex:1;}  
.cart-item-name{font-size:0.82rem;font-weight:700;color:var(--dark);font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;}  
.cart-item-color{font-size:0.7rem;color:var(--text2);margin:2px 0;font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;}  
.cart-item-price{font-size:0.88rem;font-weight:700;color:var(--gold2);font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;}  
.cart-item-del{background:none;border:none;cursor:pointer;color:var(--text2);font-size:1rem;}  
.cart-item-del:hover{color:var(--red);}  
.cart-empty{text-align:center;padding:45px 20px;color:var(--text2);font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;}  
.cart-foot{  
  padding:16px 20px;border-top:1px solid rgba(139,105,20,0.15);background:var(--off);  
}  
.cart-total{display:flex;justify-content:space-between;align-items:center;margin-bottom:12px;}  
.cart-total-lbl{font-size:0.85rem;color:var(--text2);font-weight:600;font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;}  
.cart-total-val{font-size:1.4rem;font-weight:900;color:var(--gold2);font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;}  
.btn-checkout{  
  width:100%;  
  background:linear-gradient(135deg,var(--gold),var(--gold3));  
  border:none;color:#fff;padding:12px;  
  font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;font-size:0.88rem;font-weight:700;  
  cursor:pointer;border-radius:8px;  
  box-shadow:0 4px 14px rgba(139,105,20,0.3);  
  transition:all 0.3s;  
}  
.btn-checkout:hover{box-shadow:0 7px 20px rgba(139,105,20,0.42);}  
  
/* ===== ABOUT ===== */  
.about-grid{display:grid;grid-template-columns:1fr 1fr;gap:60px;align-items:center;max-width:1100px;margin:0 auto;}  
.about-stats{display:grid;grid-template-columns:1fr 1fr;gap:12px;margin-top:22px;}  
.stat-box{  
  background:#fff;border:2px solid rgba(139,105,20,0.18);  
  border-radius:10px;padding:18px;  
  box-shadow:0 3px 12px rgba(139,105,20,0.07);  
  transition:all 0.3s;  
}  
.stat-box:hover{border-color:var(--gold);transform:translateY(-3px);}  
.stat-num{font-size:1.9rem;font-weight:900;color:var(--gold2);font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;}  
.stat-lbl{font-size:0.72rem;color:var(--text2);font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;margin-top:3px;}  
.about-visual{display:flex;align-items:center;justify-content:center;min-height:360px;}  
.about-circles{position:relative;width:300px;height:300px;}  
.ac1{position:absolute;inset:0;border-radius:50%;border:2px solid rgba(139,105,20,0.5);animation:spin 20s linear infinite;}  
.ac2{position:absolute;inset:24px;border-radius:50%;border:2px solid rgba(139,105,20,0.7);animation:spin 15s linear infinite reverse;}  
.ac3{position:absolute;inset:54px;border-radius:50%;border:2px solid var(--gold);background:radial-gradient(circle,rgba(139,105,20,0.1),transparent);}  
.ac-inner{  
  position:absolute;inset:78px;border-radius:50%;  
  background:linear-gradient(135deg,var(--gold),var(--gold2));  
  display:flex;flex-direction:column;align-items:center;justify-content:center;  
  box-shadow:0 8px 35px rgba(139,105,20,0.4);  
}  
.ac-t{font-size:3rem;font-weight:900;color:#fff;font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;}  
.ac-s{font-size:0.52rem;color:rgba(255,255,255,0.9);letter-spacing:2px;text-transform:uppercase;font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;}  
.ac-dot{position:absolute;width:9px;height:9px;background:var(--gold2);border-radius:50%;top:50%;left:50%;transform:rotate(var(--a)) translateY(-148px) translate(-50%,-50%);box-shadow:0 0 7px rgba(180,140,50,0.6);}  
@keyframes spin{from{transform:rotate(0deg)}to{transform:rotate(360deg)}}  
  
/* ===== TESTIMONIALS ===== */  
.testi-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:18px;max-width:1100px;margin:0 auto;}  
.testi-card{  
  background:var(--off);border-radius:12px;padding:24px;  
  border:1px solid rgba(139,105,20,0.12);  
  box-shadow:0 3px 14px rgba(0,0,0,0.05);  
  transition:all 0.3s;  
}  
.testi-card:hover{transform:translateY(-4px);border-color:var(--gold);}  
.testi-stars{color:#A07820;font-size:1rem;letter-spacing:2px;margin-bottom:12px;}  
.testi-text{font-size:0.86rem;color:var(--text2);line-height:1.8;font-style:italic;margin-bottom:14px;font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;}  
.testi-author{display:flex;align-items:center;gap:9px;border-top:1px solid rgba(139,105,20,0.1);padding-top:12px;}  
.testi-av{width:36px;height:36px;border-radius:50%;background:linear-gradient(135deg,var(--gold),var(--gold4));display:flex;align-items:center;justify-content:center;font-size:1rem;}  
.testi-name{font-size:0.83rem;font-weight:700;color:var(--dark);font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;}  
.testi-loc{font-size:0.7rem;color:var(--text2);font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;}  
  
/* ===== NEWSLETTER ===== */  
.newsletter{  
  padding:65px 5%;  
  background:linear-gradient(135deg,var(--gold),var(--gold2));  
  text-align:center;  
}  
.nl-title{font-size:clamp(1.4rem,3vw,2rem);font-weight:900;color:#fff;margin-bottom:7px;font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;}  
.nl-sub{font-size:0.88rem;color:rgba(255,255,255,0.9);margin-bottom:25px;font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;}  
.nl-form{display:flex;max-width:460px;margin:0 auto;border-radius:6px;overflow:hidden;box-shadow:0 6px 25px rgba(0,0,0,0.18);}  
.nl-in{flex:1;background:#fff;border:none;color:var(--dark);padding:13px 16px;font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;font-size:0.86rem;outline:none;direction:rtl;}  
.nl-btn{background:var(--dark);color:#fff;border:none;padding:13px 22px;font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;font-size:0.82rem;font-weight:700;cursor:pointer;white-space:nowrap;transition:background 0.3s;}  
.nl-btn:hover{background:#333;}  
  
/* ===== FOOTER ===== */  
footer{background:var(--dark);padding:55px 5% 22px;}  
.footer-grid{display:grid;grid-template-columns:2fr 1fr 1fr 1fr;gap:45px;margin-bottom:35px;}  
.footer-logo img{height:50px;object-fit:contain;display:block;margin-bottom:12px;}  
.footer-desc{font-size:0.78rem;color:rgba(255,255,255,0.45);line-height:1.8;font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;}  
.footer-h{font-size:0.68rem;letter-spacing:3px;color:var(--gold3);text-transform:uppercase;margin-bottom:15px;font-weight:700;font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;}  
.footer-links{list-style:none;}  
.footer-links li{margin-bottom:9px;}  
.footer-links a{color:rgba(255,255,255,0.4);font-size:0.8rem;font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;transition:color 0.3s;}  
.footer-links a:hover{color:var(--gold3);}  
.footer-bottom{border-top:1px solid rgba(255,255,255,0.08);padding-top:20px;display:flex;justify-content:space-between;flex-wrap:wrap;gap:8px;}  
.footer-copy{font-size:0.72rem;color:rgba(255,255,255,0.3);font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;}  
.footer-copy span{color:var(--gold3);}  
  
/* ===== MOBILE MENU ===== */  
.menu-bg{position:fixed;inset:0;background:rgba(0,0,0,0.5);z-index:699;opacity:0;visibility:hidden;transition:all 0.3s;}  
.menu-bg.open{opacity:1;visibility:visible;}  
.side-menu{  
  position:fixed;top:0;right:0;width:290px;max-width:85vw;height:100vh;  
  background:#fff;z-index:700;  
  transform:translateX(100%);  
  transition:transform 0.4s cubic-bezier(0.4,0,0.2,1);  
  display:flex;flex-direction:column;  
  box-shadow:-4px 0 25px rgba(0,0,0,0.12);  
}  
.side-menu.open{transform:translateX(0);}  
.side-head{  
  display:flex;align-items:center;justify-content:space-between;  
  padding:16px 18px;border-bottom:2px solid var(--gold);background:var(--off);  
}  
.side-head img{height:42px;object-fit:contain;}  
.side-close{background:none;border:none;font-size:1.3rem;color:var(--text2);cursor:pointer;}  
.side-links{list-style:none;padding:12px 0;flex:1;}  
.side-links li{border-bottom:1px solid rgba(139,105,20,0.08);}  
.side-links a{display:block;padding:14px 22px;color:var(--dark);font-size:0.92rem;font-weight:600;font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;transition:all 0.2s;}  
.side-links a:hover{background:var(--off);color:var(--gold);}  
.side-social{padding:18px;border-top:1px solid rgba(139,105,20,0.12);background:var(--off);}  
.side-social-title{font-size:0.68rem;letter-spacing:2px;color:var(--gold);text-transform:uppercase;margin-bottom:10px;font-weight:700;font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;}  
.side-social-links{display:flex;flex-direction:column;gap:8px;}  
.social-link-btn{  
  display:flex;align-items:center;gap:10px;  
  padding:9px 12px;background:#fff;  
  border:1.5px solid rgba(139,105,20,0.18);  
  border-radius:7px;color:var(--dark);  
  font-size:0.82rem;font-weight:600;font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;  
  transition:all 0.2s;  
}  
.social-link-btn:hover{border-color:var(--gold);color:var(--gold);}  
  
/* ===== TOAST ===== */  
.toast{  
  position:fixed;bottom:22px;left:50%;  
  transform:translateX(-50%) translateY(70px);  
  background:var(--dark);border:2px solid var(--gold);  
  color:var(--gold3);padding:11px 26px;  
  font-size:0.85rem;font-weight:600;font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;  
  border-radius:50px;z-index:9999;  
  transition:transform 0.4s cubic-bezier(0.34,1.56,0.64,1);  
  white-space:nowrap;  
}  
.toast.show{transform:translateX(-50%) translateY(0);}  
  
.fade-up{opacity:0;transform:translateY(22px);transition:opacity 0.6s,transform 0.6s;}  
.fade-up.visible{opacity:1;transform:translateY(0);}  
  
/* ===== RESPONSIVE ===== */  
@media(max-width:900px){  
  .hero-grid,.about-grid{grid-template-columns:1fr;text-align:center;}  
  .hero-img-wrap{order:-1;}  
  .hero-img-wrap img{max-width:300px;margin:0 auto;display:block;}  
  .modal-body{grid-template-columns:1fr;}  
  .testi-grid{grid-template-columns:1fr;}  
  .footer-grid{grid-template-columns:1fr 1fr;}  
  .nav-links{display:none;}  
  .nav-menu-btn{display:block;}  
  .features-bar{gap:15px;}  
  .sec-line{margin:0 auto;}  
}  
@media(max-width:600px){  
  .products-grid{grid-template-columns:1fr 1fr;gap:10px;}  
  .footer-grid{grid-template-columns:1fr;}  
  .form-row{grid-template-columns:1fr;}  
}  
@media(max-width:380px){.products-grid{grid-template-columns:1fr;}}  
</style>  
  
</head>  
<body>  
  
<!-- NAV -->  
  
<nav id="nav">  
  <a href="#" class="nav-logo"><img src="logo.jpeg" alt="Tempo D'or"></a>  
  <ul class="nav-links">  
    <li><a href="#products">المنتجات</a></li>  
    <li><a href="#about">عن المتجر</a></li>  
    <li><a href="#testimonials">آراء العملاء</a></li>  
    <li><a href="#footer">تواصل معنا</a></li>  
  </ul>  
  <div class="nav-right">  
    <button class="nav-cart-btn" onclick="toggleCart()">🛒 <span>السلة</span> <span class="cart-count" id="cartCount">0</span></button>  
    <button class="nav-menu-btn" onclick="toggleMenu()">☰</button>  
  </div>  
</nav>  
  
<!-- HERO -->  
  
<section class="hero">  
  <div class="hero-grid">  
    <div class="hero-text">  
      <p class="hero-eyebrow">Tempo D'or · For Watches</p>  
      <h1 class="hero-title">الوقت <span>ذهب</span><br>اختر ساعتك</h1>  
      <p class="hero-sub">أفخر الساعات العالمية بأسعار استثنائية،<br>مع ضمان الجودة والتوصيل لباب بيتك.</p>  
      <a href="#products" class="hero-btn">🕐 تصفح المجموعة</a>  
    </div>  
    <div class="hero-img-wrap">  
      <img src="hero%20card.png" alt="Tempo D'or">  
    </div>  
  </div>  
</section>  
  
<!-- FEATURES -->  
  
<div class="features-bar">  
  <div class="feat-item">🚚 توصيل سريع لجميع المدن</div>  
  <div class="feat-item">✅ ضمان الأصالة 100%</div>  
  <div class="feat-item">🔄 إرجاع خلال 7 أيام</div>  
  <div class="feat-item">💬 دعم عبر واتساب</div>  
</div>  
  
<!-- PRODUCTS -->  
  
<section class="section bg-off fade-up" id="products">  
  <div class="sec-head">  
    <p class="sec-label">تشكيلتنا</p>  
    <h2 class="sec-title">ساعات <span>مختارة</span></h2>  
    <div class="sec-line"></div>  
  </div>  
  <div class="filter-wrap">  
    <button class="filter-btn active" onclick="filterProds('all',this)">الكل</button>  
    <button class="filter-btn" onclick="filterProds('smart',this)">ذكية</button>  
    <button class="filter-btn" onclick="filterProds('sport',this)">رياضية</button>  
    <button class="filter-btn" onclick="filterProds('classic',this)">كلاسيك</button>  
  </div>  
  <div class="products-grid" id="prodsGrid"></div>  
</section>  
  
<!-- ABOUT -->  
  
<section class="section bg-white fade-up" id="about">  
  <div class="about-grid">  
    <div>  
      <p class="sec-label">من نحن</p>  
      <h2 class="sec-title">قصة <span>Tempo D'or</span></h2>  
      <div class="sec-line" style="margin:14px 0;"></div>  
      <p style="font-size:0.95rem;color:var(--text2);line-height:1.9;font-family:'SF Arabic','Geeza Pro',Tahoma,Arial,sans-serif;">نحن متجر متخصص في الساعات الفاخرة، نقدم أفضل الماركات العالمية بأسعار تنافسية مع ضمان الجودة والأصالة في كل قطعة.</p>  
      <div class="about-stats">  
        <div class="stat-box"><div class="stat-num">+500</div><div class="stat-lbl">عميل سعيد</div></div>  
        <div class="stat-box"><div class="stat-num">100%</div><div class="stat-lbl">ضمان الأصالة</div></div>  
        <div class="stat-box"><div class="stat-num">48h</div><div class="stat-lbl">توصيل سريع</div></div>  
        <div class="stat-box"><div class="stat-num">5★</div><div class="stat-lbl">تقييم العملاء</div></div>  
      </div>  
    </div>  
    <div class="about-visual">  
      <div class="about-circles">  
        <div class="ac1"></div><div class="ac2"></div><div class="ac3"></div>  
        <div class="ac-inner"><div class="ac-t">T</div><div class="ac-s">Tempo D'or</div></div>  
        <div class="ac-dot" style="--a:0deg"></div>  
        <div class="ac-dot" style="--a:45deg"></div>  
        <div class="ac-dot" style="--a:90deg"></div>  
        <div class="ac-dot" style="--a:135deg"></div>  
        <div class="ac-dot" style="--a:180deg"></div>  
        <div class="ac-dot" style="--a:225deg"></div>  
        <div class="ac-dot" style="--a:270deg"></div>  
        <div class="ac-dot" style="--a:315deg"></div>  
      </div>  
    </div>  
  </div>  
</section>  
  
<!-- TESTIMONIALS -->  
  
<section class="section bg-off fade-up" id="testimonials">  
  <div class="sec-head">  
    <p class="sec-label">آراء عملائنا</p>  
    <h2 class="sec-title">ماذا يقولون <span>عنّا</span></h2>  
    <div class="sec-line"></div>  
  </div>  
  <div class="testi-grid">  
    <div class="testi-card fade-up">  
      <div class="testi-stars">★★★★★</div>  
      <p class="testi-text">"وصلتني الساعة في أقل من يومين والجودة فاقت توقعاتي، سأكون عميلاً دائماً."</p>  
      <div class="testi-author"><div class="testi-av">👨</div><div><div class="testi-name">محمد العلي</div><div class="testi-loc">طرابلس</div></div></div>  
    </div>  
    <div class="testi-card fade-up">  
      <div class="testi-stars">★★★★★</div>  
      <p class="testi-text">"اشتريت ساعة Curren وأنا مبهوت من التصميم والتغليف الراقي، خدمة ممتازة."</p>  
      <div class="testi-author"><div class="testi-av">👩</div><div><div class="testi-name">سارة الورفلي</div><div class="testi-loc">بنغازي</div></div></div>  
    </div>  
    <div class="testi-card fade-up">  
      <div class="testi-stars">★★★★★</div>  
      <p class="testi-text">"أفضل متجر ساعات تعاملت معه، أسعار ممتازة ومنتجات أصلية 100٪."</p>  
      <div class="testi-author"><div class="testi-av">👨‍💼</div><div><div class="testi-name">خالد البغدادي</div><div class="testi-loc">مصراتة</div></div></div>  
    </div>  
  </div>  
</section>  
  
<!-- NEWSLETTER -->  
  
<div class="newsletter fade-up">  
  <h2 class="nl-title">اشترك واحصل على خصم 10%</h2>  
  <p class="nl-sub">كن أول من يعلم بالعروض والمنتجات الجديدة</p>  
  <div class="nl-form">  
    <input type="email" class="nl-in" placeholder="بريدك الإلكتروني...">  
    <button class="nl-btn" onclick="subscribeNL()">اشترك الآن</button>  
  </div>  
</div>  
  
<!-- FOOTER -->  
  
<footer id="footer">  
  <div class="footer-grid">  
    <div>  
      <a href="#" class="footer-logo"><img src="logo.jpeg" alt="Tempo D'or" style="filter:brightness(0) invert(1);opacity:0.85;"></a>  
      <p class="footer-desc">متجر Tempo D'or — وقت من ذهب. نقدم أفخر الساعات العالمية بأسعار استثنائية.</p>  
    </div>  
    <div>  
      <h4 class="footer-h">روابط</h4>  
      <ul class="footer-links">  
        <li><a href="#products">المنتجات</a></li>  
        <li><a href="#about">عن المتجر</a></li>  
        <li><a href="#testimonials">آراء العملاء</a></li>  
      </ul>  
    </div>  
    <div>  
      <h4 class="footer-h">خدماتنا</h4>  
      <ul class="footer-links">  
        <li><a href="#">سياسة الإرجاع</a></li>  
        <li><a href="#">تتبع طلبك</a></li>  
        <li><a href="#">الأسئلة الشائعة</a></li>  
      </ul>  
    </div>  
    <div>  
      <h4 class="footer-h">تواصل</h4>  
      <ul class="footer-links">  
        <li><a href="https://wa.me/218945069436">💬 واتساب</a></li>  
        <li><a href="tel:+218945069436">📞 0945069436</a></li>  
      </ul>  
    </div>  
  </div>  
  <div class="footer-bottom">  
    <p class="footer-copy">© 2025 <span>Tempo D'or</span> — جميع الحقوق محفوظة</p>  
    <p class="footer-copy">صُنع بـ ❤️ لعشاق الساعات</p>  
  </div>  
</footer>  
  
<!-- CART -->  
  
<div class="cart-bg" id="cartBg" onclick="toggleCart()"></div>  
<div class="cart-drawer" id="cartDrawer">  
  <div class="cart-head"><span class="cart-ttl">🛒 سلة المشتريات</span><button class="cart-cls" onclick="toggleCart()">×</button></div>  
  <div class="cart-items" id="cartItems"><div class="cart-empty" id="cartEmpty"><div style="font-size:3rem;margin-bottom:10px;opacity:0.3">🛒</div><p>سلتك فارغة</p></div></div>  
  <div class="cart-foot">  
    <div class="cart-total"><span class="cart-total-lbl">الإجمالي</span><span class="cart-total-val" id="cartTotal">0 LYD</span></div>  
    <button class="btn-checkout" onclick="checkoutCart()">📲 إتمام الطلب عبر واتساب</button>  
  </div>  
</div>  
  
<!-- MOBILE MENU -->  
  
<div class="menu-bg" id="menuBg" onclick="toggleMenu()"></div>  
<div class="side-menu" id="sideMenu">  
  <div class="side-head">  
    <img src="logo.jpeg" alt="Tempo D'or">  
    <button class="side-close" onclick="toggleMenu()">×</button>  
  </div>  
  <ul class="side-links">  
    <li><a href="#products" onclick="toggleMenu()">⌚ المنتجات</a></li>  
    <li><a href="#about" onclick="toggleMenu()">🏆 عن المتجر</a></li>  
    <li><a href="#testimonials" onclick="toggleMenu()">⭐ آراء العملاء</a></li>  
    <li><a href="#footer" onclick="toggleMenu()">📞 تواصل معنا</a></li>  
  </ul>  
  <div class="side-social">  
    <p class="side-social-title">تابعنا على</p>  
    <div class="side-social-links">  
      <a href="https://www.instagram.com/tempodor.ly" target="_blank" class="social-link-btn">📸 Instagram — tempodor.ly</a>  
      <a href="https://www.tiktok.com/@tempo.dor" target="_blank" class="social-link-btn">🎵 TikTok — tempo.dor</a>  
      <a href="https://facebook.com/share/1CxLkCdNHJ/" target="_blank" class="social-link-btn">👍 Facebook — Tempo D'or</a>  
      <a href="https://wa.me/218945069436" target="_blank" class="social-link-btn">💬 WhatsApp</a>  
    </div>  
  </div>  
</div>  
  
<!-- MODAL -->  
  
<div class="modal-overlay" id="modal">  
  <div class="product-modal">  
    <div class="modal-header"><span class="modal-title" id="modalTitle">تفاصيل المنتج</span><button class="modal-close" onclick="closeModal()">×</button></div>  
    <div class="modal-body" id="modalBody"></div>  
  </div>  
</div>  
  
<div class="toast" id="toast"></div>  
  
<script>  
const IMGS = {  
  poedagar:'poedagar.jpeg',  
  curren_black:'curren%20black.jpeg',  
  curren_white:'curren%20white.jpeg',  
  curren_blue:'curren%20blue.jpeg',  
  curren_skyblue:'curren%20skyblue.jpeg',  
  rolex:'rolex.jpeg',  
  hk11:'hk11.jpeg',  
};  
  
const PRODUCTS = [  
  {id:1,name:'Poedagar',cat:'classic',price:120,soldOut:true,  
   colors:['أسود','أبيض','أخضر','أزرق'],  
   cImgs:{أسود:'poedagar',أبيض:'poedagar',أخضر:'poedagar',أزرق:'poedagar'},  
   img:'poedagar',desc:'ساعة Poedagar الفاخرة، هيكل من الفولاذ المصقول وزجاج مقاوم للخدش.'},  
  {id:2,name:'Curren Chronograph',cat:'sport',price:200,sale:140,soldOut:false,  
   colors:['أزرق ملكي','أبيض','أزرق سماوي','أسود'],  
   cImgs:{'أزرق ملكي':'curren_blue','أبيض':'curren_white','أزرق سماوي':'curren_skyblue','أسود':'curren_black'},  
   img:'curren_black',desc:'ساعة Curren كرونوغراف رياضية، مقاومة للماء، حركة كوارتز دقيقة.'},  
  {id:3,name:'Rolex Day-Date',cat:'classic',price:185,sale:105,soldOut:false,  
   colors:['أبيض'],cImgs:{أبيض:'rolex'},img:'rolex',  
   desc:'ساعة Rolex Day-Date الأيقونية بالأرقام العربية، تصميم فاخر.'},  
  {id:4,name:'HK11 Pro Max',cat:'smart',price:365,soldOut:true,  
   colors:['أسود'],cImgs:{أسود:'hk11'},img:'hk11',  
   desc:'ساعة ذكية HK11 Pro Max، شاشة كبيرة، متابعة الصحة والرياضة.'},  
];  
  
const WA='218945069436';  
let cart=[], selColor={};  
  
function chex(n){return {'أسود':'#222','أبيض':'#eee','أخضر':'#2d8a4e','أزرق':'#1a5fa8','أزرق ملكي':'#1a3fa8','أزرق سماوي':'#5ab5e8'}[n]||'#888';}  
function catName(c){return {classic:'كلاسيك',sport:'رياضية',smart:'ذكية'}[c]||c;}  
  
function renderProds(filter='all'){  
  const g=document.getElementById('prodsGrid');  
  const list=filter==='all'?PRODUCTS:PRODUCTS.filter(p=>p.cat===filter);  
  g.innerHTML=list.map(p=>{  
    const dots=p.colors.map(c=>`<div class="color-dot" style="background:${chex(c)}" title="${c}"></div>`).join('');  
    let ph='';  
    if(p.soldOut) ph=`<span class="price-old">${p.price} LYD</span><span class="price-sold">نفدت الكمية</span>`;  
    else if(p.sale) ph=`<span class="price-old">${p.price} LYD</span><span class="price-sale">${p.sale} LYD</span>`;  
    else ph=`<span class="price-new">${p.price} LYD</span>`;  
    return `<div class="product-card" onclick="openModal(${p.id})">  
      ${p.soldOut?'<div class="card-badge badge-sold">نفدت الكمية</div>':p.sale?'<div class="card-badge badge-sale">تخفيض 🔥</div>':''}  
      <div class="card-img">  
        <img src="${IMGS[p.img]}" alt="${p.name}" loading="lazy">  
        ${p.soldOut?'<div class="sold-overlay">❌ نفدت الكمية</div>':''}  
      </div>  
      <div class="color-dots">${dots}</div>  
      <div class="card-info">  
        <div class="card-cat">${catName(p.cat)}</div>  
        <div class="card-name">${p.name}</div>  
        <div class="card-price">${ph}</div>  
        <div class="card-actions">  
          <button class="btn-order" onclick="event.stopPropagation();openModal(${p.id})" ${p.soldOut?'disabled':''}>  
            ${p.soldOut?'نفدت الكمية':'🛒 اطلب الآن'}  
          </button>  
          <button class="btn-cart" onclick="event.stopPropagation();addCart(${p.id})" ${p.soldOut?'disabled':''}>＋</button>  
        </div>  
      </div>  
    </div>`;  
  }).join('');  
  g.querySelectorAll('.product-card').forEach(el=>obs.observe(el));  
}  
  
function filterProds(cat,btn){  
  document.querySelectorAll('.filter-btn').forEach(b=>b.classList.remove('active'));  
  btn.classList.add('active');  
  renderProds(cat);  
}  
  
function openModal(id){  
  const p=PRODUCTS.find(x=>x.id===id);  
  if(!p)return;  
  selColor[id]=p.colors[0];  
  document.getElementById('modalTitle').textContent=p.name;  
  let ph='';  
  if(p.soldOut) ph=`<span class="modal-p-old">${p.price} LYD</span><span class="modal-p-sold">❌ نفدت الكمية</span>`;  
  else if(p.sale) ph=`<span class="modal-p-old">${p.price} LYD</span><span class="modal-p-sale">${p.sale} LYD</span>`;  
  else ph=`<span class="modal-p-new">${p.price} LYD</span>`;  
  const cbts=p.colors.map(c=>`<button class="color-opt ${c===p.colors[0]?'active':''}" onclick="pickColor(${id},'${c}',this)">${c}</button>`).join('');  
  document.getElementById('modalBody').innerHTML=`  
    <div class="modal-img"><img src="${IMGS[p.img]}" alt="${p.name}" id="mImg${id}"></div>  
    <div class="modal-info">  
      <div class="modal-cat">${catName(p.cat)}</div>  
      <div class="modal-name">${p.name}</div>  
      <p class="modal-desc">${p.desc}</p>  
      <div class="modal-prices">${ph}</div>  
      <div class="color-sec">  
        <div class="color-lbl">اختر اللون</div>  
        <div class="color-opts" id="co${id}">${cbts}</div>  
      </div>  
      ${!p.soldOut?`  
      <div class="form-row">  
        <div class="form-g"><label class="form-lbl">الاسم</label><input type="text" class="form-in" id="oName" placeholder="اسمك الكامل"></div>  
        <div class="form-g"><label class="form-lbl">الجوال</label><input type="tel" class="form-in" id="oPhone" placeholder="09xxxxxxxx"></div>  
      </div>  
      <div class="form-g"><label class="form-lbl">المدينة</label>  
        <select class="form-sel" id="oCity">  
          <option>اختر المدينة</option>  
          <option>طرابلس</option><option>بنغازي</option><option>مصراتة</option>  
          <option>الزاوية</option><option>سبها</option><option>البيضاء</option>  
          <option>زليتن</option><option>الخمس</option><option>أخرى</option>  
        </select>  
      </div>  
      <div class="form-g"><label class="form-lbl">العنوان</label><input type="text" class="form-in" id="oAddr" placeholder="الحي، الشارع..."></div>  
      <button class="btn-submit" onclick="submitOrder(${id})">📲 إرسال الطلب عبر واتساب</button>`  
      :'<div class="sold-msg">⚠️ هذا المنتج نفدت كميته حالياً</div>'}  
    </div>`;  
  document.getElementById('modal').classList.add('open');  
  document.body.style.overflow='hidden';  
}  
  
function pickColor(id,c,btn){  
  selColor[id]=c;  
  document.querySelectorAll(`#co${id} .color-opt`).forEach(b=>b.classList.remove('active'));  
  btn.classList.add('active');  
  const p=PRODUCTS.find(x=>x.id===id);  
  if(p&&p.cImgs&&p.cImgs[c]){  
    const img=document.getElementById(`mImg${id}`);  
    if(img){img.style.opacity=0;setTimeout(()=>{img.src=IMGS[p.cImgs[c]];img.style.opacity=1;},200);}  
  }  
}  
  
function closeModal(){document.getElementById('modal').classList.remove('open');document.body.style.overflow='';}  
  
function submitOrder(id){  
  const p=PRODUCTS.find(x=>x.id===id);  
  const name=(document.getElementById('oName')?.value||'').trim();  
  const phone=(document.getElementById('oPhone')?.value||'').trim();  
  const city=document.getElementById('oCity')?.value;  
  const addr=(document.getElementById('oAddr')?.value||'').trim();  
  if(!name||!phone||city==='اختر المدينة'||!addr){showToast('⚠️ يرجى ملء جميع الحقول');return;}  
  const color=selColor[id]||p.colors[0];  
  const price=p.sale||p.price;  
  const msg=`🕐 *طلب جديد - Tempo D'or*%0A%0A⌚ *الساعة:* ${p.name}%0A🎨 *اللون:* ${color}%0A💰 *السعر:* ${price} LYD%0A%0A👤 *الاسم:* ${name}%0A📞 *الجوال:* ${phone}%0A📍 *المدينة:* ${city}%0A🏠 *العنوان:* ${addr}`;  
  window.open(`https://wa.me/${WA}?text=${msg}`,'_blank');  
  closeModal();  
  showToast('✅ تم تحويلك لواتساب!');  
}  
  
function addCart(id){  
  const p=PRODUCTS.find(x=>x.id===id);  
  if(p.soldOut){showToast('❌ نفدت الكمية');return;}  
  const ex=cart.find(x=>x.id===id);  
  if(ex)ex.qty++;  
  else cart.push({...p,qty:1,chosenColor:p.colors[0]});  
  updateCart();  
  showToast(`✅ تمت إضافة "${p.name}"`);  
}  
  
function updateCart(){  
  const cnt=cart.reduce((s,x)=>s+x.qty,0);  
  document.getElementById('cartCount').textContent=cnt;  
  const total=cart.reduce((s,x)=>s+(x.sale||x.price)*x.qty,0);  
  document.getElementById('cartTotal').textContent=total.toLocaleString()+' LYD';  
  const con=document.getElementById('cartItems');  
  const emp=document.getElementById('cartEmpty');  
  con.querySelectorAll('.cart-item').forEach(e=>e.remove());  
  if(!cart.length){emp.style.display='block';return;}  
  emp.style.display='none';  
  cart.forEach(item=>{  
    const d=document.createElement('div');  
    d.className='cart-item';  
    d.innerHTML=`<img class="cart-item-img" src="${IMGS[item.img]}" alt="${item.name}">  
    <div class="cart-item-info">  
      <div class="cart-item-name">${item.name}${item.qty>1?' ×'+item.qty:''}</div>  
      <div class="cart-item-color">اللون: ${item.chosenColor}</div>  
      <div class="cart-item-price">${((item.sale||item.price)*item.qty).toLocaleString()} LYD</div>  
    </div>  
    <button class="cart-item-del" onclick="removeCart(${item.id})">🗑</button>`;  
    con.insertBefore(d,emp);  
  });  
}  
  
function removeCart(id){cart=cart.filter(x=>x.id!==id);updateCart();}  
  
function toggleCart(){  
  document.getElementById('cartDrawer').classList.toggle('open');  
  document.getElementById('cartBg').classList.toggle('open');  
}  
  
function checkoutCart(){  
  if(!cart.length){showToast('⚠️ أضف منتجاً أولاً');return;}  
  let msg=`🛒 *طلب سلة - Tempo D'or*%0A%0A`;  
  cart.forEach(i=>{msg+=`⌚ ${i.name} (${i.chosenColor}) ×${i.qty} = ${(i.sale||i.price)*i.qty} LYD%0A`;});  
  const total=cart.reduce((s,x)=>s+(x.sale||x.price)*x.qty,0);  
  msg+=`%0A💰 *الإجمالي:* ${total} LYD%0A%0Aيرجى إرسال: الاسم، الجوال، المدينة، العنوان`;  
  window.open(`https://wa.me/${WA}?text=${msg}`,'_blank');  
  toggleCart();  
}  
  
function toggleMenu(){  
  document.getElementById('sideMenu').classList.toggle('open');  
  document.getElementById('menuBg').classList.toggle('open');  
}  
  
window.addEventListener('scroll',()=>document.getElementById('nav').classList.toggle('scrolled',scrollY>60));  
  
const obs=new IntersectionObserver(es=>es.forEach(e=>{if(e.isIntersecting)e.target.classList.add('visible');}),{threshold:0.1});  
document.querySelectorAll('.fade-up').forEach(el=>obs.observe(el));  
  
function showToast(msg){  
  const t=document.getElementById('toast');  
  t.textContent=msg;t.classList.add('show');  
  setTimeout(()=>t.classList.remove('show'),3000);  
}  
  
function subscribeNL(){  
  const i=document.querySelector('.nl-in');  
  if(!i.value||!i.value.includes('@')){showToast('⚠️ أدخل بريداً صحيحاً');return;}  
  showToast('🎁 تم الاشتراك! ستصلك كوبون الخصم');i.value='';  
}  
  
document.getElementById('modal').addEventListener('click',function(e){if(e.target===this)closeModal();});  
renderProds();  
</script>  
  
</body>  
</html>  
