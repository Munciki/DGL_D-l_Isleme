# DGL_D-l_Isleme
Repo üzerinden modelin nasıl oluşturulabileceği (adım adım açıklama)
öncelikle bir https linkini vcode'dan okutuyoruz, ve linkin bize txt haliyle geliyor, bu txt halinin icini okutarak yani dosya okuma islemi yaparak veriyi bagliyoruz 
veri baglandiktan sonra ne yapmamiz gerektiğine karar veriyoruz ve bu sayede,elimizde işlem yapabilecegimiz bir veri setimiz oluyor.
# Veri setinin hangi amaçla kullanılabileceği
Bu veri seti Davadaki Metinlerle davadaki Tanıkların ne kadar uyumlu cümleler kullandıgını kendi içerisinde çözer ve bunun cosine sumilarity sini ve ham metnin Zipf yasasina uygun haliylede kelimelerin nerelerde nasıl kullanıldıgı ne coklukla databasesi gözükmektedir.

# Gerekli kütüphaneler ve kurulum talimatları
import nltk
import string
import csv
import gensim
from nltk.corpus import stopwords
from nltk.tokenize import word_tokenize, sent_tokenize
from nltk.stem import WordNetLemmatizer, PorterStemmer
from sklearn.feature_extraction.text import TfidfVectorizer
from gensim.models import Word2Vec

# Kaynak: Veri seti nereden ve nasıl indirildi? Detaylı açıklayınız
Veri setini CourtListener ve Oyez'den cektim yardim alarak yazdiğim bi kodla bu sitelerin icindeki pdfleri okuyan ve bunu txt haline getiren programım sayesinde
bu veri setlerini indirdim ve bunu kullandım aksi takdirde böyle yapmasaydim bu siteler 403 koduyla korundugu icin veri getirtemezdim.

# Boyut: Toplam kaç döküman içeriyor? Kaç MB? Hangi formatta (HTML, JSON,vs.)?
Toplam 2 döküman içeriyor, 10mgb Veri iceriyor, Html ve Txt Formatında

# Örnek: Ham veriden kısa bir örnek parça paylaşınız. Bu örnek üzerinden veri
# içeriğini detaylıca açıklayınız. Temizleme sürecinin anlaşılması açısından
# önemlidir.
![resim](https://github.com/user-attachments/assets/4bcf3da3-269c-43bd-b7bd-dd65e5df6a61)



# Vektör çıktılarından örnekler PDF raporda paylaşılmalıdır. Her model için,
# örneğin belirli bir önemli kelime seçilerek (verdiğim örnek kodda olduğu gibi), bu
# kelimenin vektör uzayındaki en yakın anlamlı (benzer) 5 kelimesi raporda
# sunulabilir. Ayrıca, elde edilen modellerin temel özellikleri bu örnekler üzerinden
# kısaca açıklanmalıdır. Hangi modelin daha başarılı olmasını bekliyorsunuz
# neden?
Stem modellerimin daha başarılı olması gerke cünkü cok az dosya var, en hızlı sekilde yapabilir.

