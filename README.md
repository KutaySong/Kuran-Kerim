# Kuran-Kerim
Allah azze ve celle'nin içinde şüphe olmayan son kitabı ile ilgi çalışmalarım

# Arapça Klavye 
Q klavye'ye alışkın insanlar için temel Arapça (esresiz ötresiz) yazmaya yarayan yazılımcık.(script)

# Kullanım
Sade:
عو غ ظ ض ا خ ي ت ر ث ص ز
 إ ش ل ق ك ه لا ف د س ع 
  ط ة م ن ب و ج ح ذ

Shift:
غ ب ء آ ع ى ط ر أ ض ك
 إ ش ل ك ج ح ق ف ض ص ء
  ج ة م ن ب ؤ ج خ ز

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

EnableArabic := 0
^6:: 
EnableArabic := !EnableArabic 
Return

#If winActive("Studio") && EnableArabic
^!e::آ
^!a::ى
^!h::ة
^!s::ث
^!t::ث
^!y::ئ
^!z::ظ

a::ع
A::ء
b::ب
c::ج
ç::ط
Ç::ج
d::د
D::ض
e::ث
E::أ
f::ف
g::Send, لا
G::ق
ğ::غ
h::ه
H::ح
ı::ا
I::آ
SC028::إ
j::ك
J::ج
k::ق
K::ك
l::ل
m::م
n::ن
o::ض
O::ء
ö::ة
p::ظ
P::ب
q::ز
Q::ك
r::ر
s::س
S::ص
ş::ش
t::ت 
T::ط
u::خ     
U::ع      
ü::Send, عو
v::و
V::ؤ
w::ص
W::ض
x::ح
X::خ
y::ي
Y::ى
z::ذ
Z::ز

^l::^l
^z::^z
!ı::!ı
!k::!k
#If
