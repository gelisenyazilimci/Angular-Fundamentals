
# Angular'ın Temel Yapı Taşları

---

## 📦 Modules (Modüller)

- Angular'da **modül yapısı**, uygulama bileşenlerini (components, services vb.) gruplandırarak daha düzenli bir yapı oluşturmayı sağlar.
- **Modüller**, uygulamanın belirli bölümlerini bir araya getirerek bir bütün olarak çalışmasını mümkün kılar.
- **Lazy Loading (Tembel Yükleme)** desteği ile yalnızca ihtiyaç duyulan modüller yüklenir, böylece performans artışı sağlanır.
- **Dependency Injection (Bağımlılık Enjeksiyonu)** kullanarak modüller arasında bağımlılıklar yönetilir, bu da test edilebilirlik ve bakım açısından avantaj sağlar.
- Bir modül, başka bir modülü **import** etmediği sürece, içindeki bileşenlere diğer modüllerden erişilemez.

---

## 🎨 Components (Bileşenler)

- **Component'ler**, kullanıcı arayüzünü oluşturan ve veri modeliyle etkileşim kurarak ekranı yöneten temel yapılardır.
- Yapısal olarak **HTML, TypeScript ve CSS dosyalarından** oluşurlar.
- Eğer bir **ürün listesi sayfası (Products Page)** oluşturmak istiyorsanız, **component** kullanmanız gerekir.
- Veri modelini görüntülemek ve güncellemek için **Data Binding** mekanizmasını kullanırlar.
- **Dependency Injection** ile ihtiyaç duydukları servislerin **instance**'larını alabilirler.
- Tipik bir Angular uygulaması, birbirleriyle etkileşim halinde olan **birden fazla component** içererek dinamik ve etkileşimli hale gelir.

---

## 🔗 Data Binding (Veri Bağlama)

- **Data Binding**, Angular'da veri modeli ile şablonlar (templates) arasındaki veri akışını yönetir.
- Böylece, uygulamadaki veri değişiklikleri otomatik olarak ekrana yansıtılır.
- **Tek yönlü ve çift yönlü (Two-Way Data Binding) veri bağlama** desteklenir:
    - **Tek yönlü bağlama**: Veri yalnızca bileşenden şablona akar.
    - **Çift yönlü bağlama**: Veri hem bileşenden şablona hem de şablondan bileşene akar.
- **Event Binding** ve **Property Binding** mekanizmaları ile veri güncellemeleri sağlanır.

---

## 🏗️ Dependency Injection (Bağımlılık Enjeksiyonu)

- **Dependency Injection (DI)**, Angular’ın temel tasarım kalıplarından biridir.
- Bileşenler ve servisler arasındaki bağımlılıkları yöneterek, kodun **daha modüler, esnek ve test edilebilir** olmasını sağlar.
- DI sayesinde, bileşenler doğrudan bağımlılık yaratmaz, bunun yerine ihtiyaç duydukları servisleri **enjekte edilir**.

---

## 📜 Directives (Yönergeler)

- **Directive'ler**, HTML elemanlarının davranışlarını ve görünümlerini değiştirmek için kullanılan özel etiketlerdir.
- Angular'daki **en önemli Directives türleri**:
    - **Yapısal Direktifler (`*ngIf`, `*ngFor`, `*ngSwitch`)** → DOM öğelerini ekleyip kaldırır.
    - **Öznitelik Direktifleri (`ngClass`, `ngStyle`)** → HTML elemanlarının stillerini veya özelliklerini değiştirir.
    - **Özel Direktifler** → Kullanıcı tarafından tanımlanmış işlevleri gerçekleştirmek için yazılabilir.

---

## 📌 Decorators (Dekoratörler)

- **Decorator'lar**, TypeScript’in bir özelliği olup Angular tarafından sıkça kullanılır.
- **Class'lara veya class üyelerine meta veriler ekleyerek** onların davranışlarını belirlememizi sağlar.
- Örnekler:
    - `@Component` → Bir sınıfı bir bileşen olarak tanımlar.
    - `@Injectable` → Bir sınıfın bir servis olduğunu belirtir.
    - `@NgModule` → Bir sınıfı bir modül olarak işaretler.

---

## 🔧 Services (Servisler)

- **Services**, genellikle **API bağlantıları, iş mantığı (business logic) ve bileşenler arası iletişim** gibi işlemleri gerçekleştirmek için kullanılır.
- Bileşenler **hafif** ve **yalnızca UI odaklı** olmalıdır, karmaşık işlemler **servislerde** tanımlanmalıdır.
- `@Injectable` dekoratörü ile işaretlenerek **Dependency Injection** mekanizması içinde kullanılabilir.

---

## 🏗️ Templates (Şablonlar)

- **Templates**, bileşenlerin HTML kısmıdır ve kullanıcı arayüzünü tanımlar.
- İçerisinde **standart HTML etiketleri, Angular Directives, Pipe'lar ve Data Binding mekanizmaları** bulunabilir.
- **Veri modeline dinamik olarak bağlanarak**, içeriğin değiştiğinde otomatik olarak güncellenmesini sağlar.

---

## 🔒 Guards (Koruma Mekanizmaları)

- **Guards**, Angular uygulamasında sayfa yönlendirmelerini (routing) kontrol etmek için kullanılır.
- Örneğin, yalnızca giriş yapmış kullanıcıların belirli bir sayfaya erişmesini sağlamak için **AuthGuard** kullanılabilir.
- **Başlıca Guard türleri**:
    - `CanActivate` → Sayfanın açılıp açılamayacağını kontrol eder.
    - `CanDeactivate` → Kullanıcı sayfadan çıkmadan önce uyarılar vermek için kullanılır.
    - `Resolve` → Sayfa açılmadan önce verileri yüklemek için kullanılır.

---

## 🔄 Pipes (Boru Hatları)

- **Pipes**, verilerin görüntülenmeden önce belirli bir biçime dönüştürülmesini sağlar.
- **Örnekler**:
    - `date | currency | uppercase | lowercase | percent | json`
- Özel Pipe'lar da oluşturularak ihtiyaca yönelik veri formatlama işlemleri yapılabilir.

---