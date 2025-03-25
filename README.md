# Kuran-Kerim
Allah azze ve celle'nin içinde şüphe olmayan son kitabı ile ilgi çalışmalarım

# Arapça Klavye 
Q klavye'ye alışkın insanlar için temel Arapça (esresiz ötresiz) yazmaya yarayan yazılımcık.(script)

![Alt Text](KlavyeYerlesimi.jpg?raw=true "ScreenShot")

# Kullanım
Sade:
; عو غ ظ ض ا خ ي ت ر أ ص ذ
;  إ ش ل ق ك ه ح ف د س ع
;   ط ث م ن ب و ج لا ز

Shift:
; غ ب ء آ ع ى ط ر آ ض ك
;  ئ ش ل ك ج ة خ ف ض ص ء
;   ج ث م ن ب ؤ ج ق ظ

SağAlt(Ctrl+Alt):
e:آ s:ث y:ئ a:ى t:ث h:ة z:ظ  


# Kurulum
Aşağıdaki bağıntıdan klavye tuşlarını değiştirmeye yarayan programı kuruyoruz (v1.1)
https://www.autohotkey.com/
Buradan aşağıyı .AHK tipi boş bir dosya oluşturup 
içine kopyalıyoruz. Sonra dosyayı tıklayıp çalıştırıyoruz.
Saatin yanına 'H' simgesi ile paketçik oluştuysa. 
Ctrl+6 ile özelliği aç kapa yapabiliriz.
(İlk çalıştığında özellik kapalıdır.) 


# Yazılım (AHK dosyasının içerisi)
#NoEnv  
SendMode Input  
SetTitleMatchMode, 2
DetectHiddenWindows On


;.............................................................
;   Arapça  
;.............................................................
EnableArabic := 0
^6:: 
EnableArabic := !EnableArabic 
Return

#If winActive("Studio") && EnableArabic
;*Alt:: SendInput {Alt}{Blind}

^!e::آ
^!a::ى
^!h::ة
^!s::ث
^!t::ث
^!y::ئ
^!z::ظ

a::Send,ع
A::ء
b::Send,ب
c::Send,ج
ç::Send,ط
Ç::Send,ج
d::Send,د
D::ض
e::Send,أ
E::آ
f::Send,ف
g::Send,ح
G::خ
ğ::Send,غ
h::Send,ه
H::ة
ı::Send,ا
I::Send,آ
SC028::Send,إ
+SC028::Send,ئ
j::Send,ك
J::ج
k::Send,ق
K::ك
l::Send,ل
m::Send,م
n::Send,ن
o::Send,ض
O::ء
ö::Send,ث
p::Send,ظ
P::ب
q::Send,ذ
Q::ك
r::Send,ر
s::Send,س
S::ص
ş::Send,ش
t::Send,ت 
T::ط
u::Send,خ     
U::ع  
ü::Send, عو
v::Send,و
V::ؤ
w::Send,ص
W::ض
x::Send, لا
X::ق
y::Send,ي
Y::ى
z::Send,ز
Z::ظ

#If
