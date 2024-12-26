1. [Temel Angular Yapısı](#temel-angular-yapısı)
2. [Data Binding ve Event Binding](#data-binding-ve-event-binding)
3. [Angular Routing](#angular-routing)
4. [Dependency Injection (DI)](#dependency-injection-di)
5. [Forms](#forms)
6. [Services ve HTTP Istekleri](#services-ve-http-istekleri)
7. [Pipes](#pipes)
8. [Directives](#directives)
9. [Angular CLI (Command Line Interface)](#angular-cli-command-line-interface)
10. [State Management](#state-management)
11. [Testing](#testing)
12. [Performance Optimization](#performance-optimization)
13. [Internationalization (i18n) ve Localization (l10n)](#internationalization-i18n-ve-localization-l10n)
14. [Security](#security)
15. [Progressive Web App (PWA)](#progressive-web-app-pwa)
16. [Angular Universal (SSR)](#angular-universal-ssr)
17. [Angular Material](#angular-material)
18. [Build ve Deployment](#build-ve-deployment)
19. [Module Federation](#module-federation)
20. [Custom Decorators](#custom-decorators)
21. [WebSockets](#websockets)
22. [Code Splitting](#code-splitting)
23. [Service Worker Caching](#service-worker-caching)
24. [Web Components](#web-components)
25. [Angular CLI Custom Schematics](#angular-cli-custom-schematics)
26. [Angular Elements](#angular-elements)
27. [Stateful Component Design](#stateful-component-design)
28. [Complex Form Controls](#complex-form-controls)
29. [Angular Server-Side Rendering (SSR) ve Angular Universal](#angular-server-side-rendering-ssr-ve-angular-universal)
30. [Dynamic Components Component Factories](#dynamic-components-component-factories)
31. [Advanced Routing](#advanced-routing)
32. [Global Error Handling](#global-error-handling)
33. [Global State Management](#global-state-management)
34. [CSS Preprocessing](#css-preprocessing)
35. [Modular Architecture Micro Frontends](#modular-architecture-micro-frontends)
36. [Custom Decorators](#custom-decorators)
37. [WebSockets](#websockets)
38. [Code Splitting](#code-splitting)
39. [Web Components](#web-components)
40. [Angular CLI Custom Schematics](#angular-cli-custom-schematics)
41. [Angular Elements](#angular-elements)
42. [Stateful Component Design](#stateful-component-design)

## Temel Angular Yapısı

Angular, modern web uygulamaları geliştirmek için kullanılan açık kaynaklı bir framework'tür. **Modüler** ve **bileşen tabanlı** yapısı sayesinde, geliştiricilere sürdürülebilir ve ölçeklenebilir projeler oluşturma imkanı tanır. Temel Angular yapısı, uygulamanın tüm bileşenlerini mantıklı bir şekilde organize eden ve bağımsız modüller halinde çalışan bir mimariye dayanır.

#### 1. **NgModules (Modüller)**

Angular uygulamaları, en temelinde **modüller (NgModules)** ile organize edilir. Modüller, Angular uygulamalarının **bileşenler**, **direktifler**, **borular (pipes)** ve **servisler** gibi öğelerini bir arada tutar. Bir Angular uygulamasında genellikle **root modülü** (`AppModule`) ve uygulamanın farklı bölümleri için **özelleşmiş modüller** (feature modules) bulunur.

Her bir modül, aşağıdaki öğeleri içerir:
- **Declarations**: Uygulamanın bileşenlerini, direktiflerini ve borularını tanımlar.
- **Imports**: Başka modülleri içeri aktarır. Örneğin, `FormsModule`, `HttpClientModule` gibi.
- **Providers**: Servislerin, bağımlılıkların veya singleton nesnelerin tanımlandığı yerdir.
- **Bootstrap**: Uygulamanın ana bileşenini başlatan kısımdır (genellikle `AppComponent`).

NgModules, Angular'ın **dependency injection (DI)** sistemini kullanarak bileşenler ve servisler arasındaki bağımlılıkları yönetir. Bu sayede uygulama daha modüler, sürdürülebilir ve test edilebilir hale gelir.

#### 2. **Components (Bileşenler)**

Bileşenler, Angular uygulamalarının **temel yapı taşlarıdır**. Her bileşen, HTML şablonu, stil ve işlevsel iş mantığını içerir. Bir bileşen, bir kullanıcının görünen kısmı olan UI ile etkileşime girer. 

Her bileşen şu öğelerden oluşur:
- **Component Class**: Bileşenin iş mantığını ve veri işlemlerini içerir. TypeScript sınıfı olarak yazılır.
- **Template**: Kullanıcıya gösterilen HTML şablonu. Angular, bu şablonları **data binding** ve **event binding** ile dinamik hale getirir.
- **Styles**: Bileşenin görsel düzenini tanımlar. Her bileşenin stil dosyası bağımsız olabilir.
- **Selector**: Bileşenin HTML'de kullanıldığı etiketi tanımlar.

Bir bileşen, genellikle bir diğer bileşeni içerebilir. Bu, **component hierarchy (bileşen hiyerarşisi)** oluşturur ve uygulamanın UI'ını organize eder.

#### 3. **Services ve Dependency Injection (DI)**

Angular'da **servisler**, genellikle **iş mantığı** ve **veri yönetimi** gibi uygulamanın genel işlevselliğini sağlar. Servisler, API istekleri, veri işleme, veya iş mantığının yönetilmesi gibi sorumluluklara sahiptir. 

**Dependency Injection (DI)**, Angular’ın en güçlü özelliklerinden biridir. Servisler, bileşenler aracılığıyla **bağımlılık enjeksiyonu (DI)** kullanılarak sağlanır. Bu, uygulama geliştirme sırasında:
- Kodun daha modüler ve esnek hale gelmesini sağlar.
- Test edilebilirliği artırır (unit testlerde bağımlılıkların kolayca mocklanmasını sağlar).

Angular, servisleri ve diğer bağımlılıkları **constructor** aracılığıyla bileşenlere veya diğer servislere enjekte eder.

#### 4. **Directives (Direktifler)**

Direktifler, Angular uygulamalarındaki **HTML elemanlarını** dönüştüren veya onları manipüle eden özel işaretlerdir. Direktifler, **yapısal direktifler** ve **öznitelik direktifleri** olarak ikiye ayrılır:
- **Yapısal Direktifler**: DOM yapısının değiştirilmesine olanak tanır. Örneğin, `*ngIf` (koşullu render) ve `*ngFor` (döngü ile render) direktifleri.
- **Öznitelik Direktifleri**: Var olan elemanlara stil veya davranış ekler. Örneğin, `ngClass`, `ngStyle` gibi direktifler.

Direktifler, HTML şablonlarında bileşenler gibi etkileşim sağlayarak Angular’ın **declarative programming (deklaratif programlama)** yaklaşımını destekler.

#### 5. **Pipes (Borular)**

Pipes, Angular’da veri dönüştürme işlemleri için kullanılır. Bir **pipe**, veriyi şablonlarda **dönüştürmek** için bir işlevsellik sağlar. Örneğin, bir tarihi istediğiniz formatta göstermek için `date` borusu, sayısal veriyi biçimlendirmek için `currency` borusu kullanabilirsiniz.

- **Built-in Pipes**: Angular, `date`, `currency`, `json`, `slice` gibi birçok yerleşik boru sunar.
- **Custom Pipes**: Kendi özel borularınızı yazabilir ve uygulamanızdaki veriyi özgün bir şekilde işleyebilirsiniz.

Pipes, veriyi yalnızca görsel düzeyde dönüştürür ve **performans optimizasyonu** sağlar çünkü yalnızca verinin gerçekten değiştiği durumlarda çalışır.

#### 6. **Routing (Yönlendirme)**

Angular'da **yönlendirme (routing)**, farklı bileşenler arasında geçişi yönetir. Uygulamanın sayfa yapısını, URL yapısına uygun şekilde dinamik olarak yönetir. **Angular Router**, URL'lere dayalı olarak belirli bileşenleri yükler ve **single-page application (SPA)** yapısında kullanıcı etkileşimini yönetir.

Yönlendirme, Angular’da:
- **RouterModule** ile yapılandırılır.
- **Routes**: Uygulama içinde hangi URL'nin hangi bileşeni göstereceğini belirler.
- **ActivatedRoute**: Yönlendirme sırasında parametreleri almak için kullanılır.
  
Routing ayrıca, **lazy loading** ve **route guards** gibi gelişmiş özellikler sunarak, uygulamanın **performansını** artırır ve **güvenliğini** sağlar.

---
## Data Binding ve Event Binding

**Data Binding (Veri Bağlama)** ve **Event Binding (Olay Bağlama)**, Angular uygulamalarında bileşenler ile şablonlar (template) arasındaki etkileşimi yönetmek için kullanılan temel tekniklerdir. Bu bağlama mekanizmaları, veri akışını kontrol eder ve kullanıcı etkileşimini bileşenlere taşır. Angular, **tek yönlü** ve **çift yönlü** veri bağlama seçenekleri sunarak dinamik, kullanıcı dostu uygulamalar geliştirmenizi sağlar.

#### 1. **Data Binding (Veri Bağlama)**

Data Binding, bileşen ve şablon arasındaki veri akışını yönetir. Angular'da farklı veri bağlama türleri vardır:

- **One-Way Data Binding (Tek Yönlü Veri Bağlama)**: Verinin sadece bir yönde (bileşenden şablona veya şablondan bileşene) akması sağlanır.
  - **Interpolation (İnterpolasyon)**: Bileşenin TypeScript sınıfındaki veriler, HTML şablonunda dinamik olarak gösterilir. Örnek: 
    ```html
    <h1>{{ title }}</h1>
    ```
    Burada `title` değişkeni, bileşenin TypeScript dosyasındaki bir değeri yansıtır.

  - **Property Binding (Özellik Bağlama)**: HTML elemanlarının özelliklerine (attributes) veri bağlamak için kullanılır. Bir bileşenin verisi, HTML elemanının özelliklerine atanır. Örnek:
    ```html
    <img [src]="imageUrl" />
    ```
    Burada `src`, `imageUrl` adlı bileşen değişkenine bağlıdır.

  - **Class Binding (Sınıf Bağlama)**: HTML elemanına dinamik sınıflar (CSS sınıfları) eklemek için kullanılır. Örnek:
    ```html
    <div [class.active]="isActive"></div>
    ```
    Burada `isActive` değişkeni true olduğunda `active` sınıfı eklenir.

  - **Style Binding (Stil Bağlama)**: Dinamik olarak stil özelliklerini değiştirmek için kullanılır. Örnek:
    ```html
    <div [style.background-color]="bgColor"></div>
    ```
    Burada `bgColor`, bileşenin TypeScript dosyasındaki bir değeri yansıtır.

- **Two-Way Data Binding (Çift Yönlü Veri Bağlama)**: Veri, bileşenden şablona ve şablondan bileşene doğru akabilir. Bu, özellikle form elemanlarında yaygın olarak kullanılır.
  - Angular'da **two-way binding** için `[(ngModel)]` kullanılır. Bu, bir değişkenin hem görsel olarak şablonda gösterilmesini hem de kullanıcının girdiği veriyi almasını sağlar. Örnek:
    ```html
    <input [(ngModel)]="name" />
    <p>{{ name }}</p>
    ```
    Burada `name` değişkeni, her iki yönde de veri akışını sağlar.

#### 2. **Event Binding (Olay Bağlama)**

Event Binding, kullanıcı etkileşimlerinden (butona tıklama, form gönderme, vs.) gelen olayları bileşenlerdeki işlevlere bağlamayı sağlar. Angular, HTML elementlerine olay dinleyicileri eklemek için **event binding** kullanır. Bu, kullanıcı etkileşimlerinin Angular bileşenlerine aktarılmasına olanak tanır.

- **Event Binding**: HTML elementlerine kullanıcı etkileşimi ile tetiklenen işlevleri bağlamak için kullanılır. Örnek:
  ```html
  <button (click)="onClick()">Click me</button>
  ```
  Burada `(click)`, `onClick()` metodu ile ilişkilendirilmiştir ve kullanıcı butona tıkladığında bu metod çağrılır.

- **Event Binding ile Parametre Aktarma**: Olaylar genellikle parametre alabilir. Parametreler, olay nesnesi veya bileşenin TypeScript sınıfındaki diğer verilere referanslar olabilir. Örnek:
  ```html
  <button (click)="onClick($event)">Click me</button>
  ```
  Burada `$event`, DOM olay nesnesini temsil eder ve `onClick` metoduna gönderilir.

#### 3. **Event Binding ve Property Binding Arasındaki Fark**

- **Property Binding**: HTML elemanlarının özelliklerine veri bağlar, yani şablon tarafındaki özelliklerin dinamik olarak bileşenin sınıfındaki verilere bağlanmasını sağlar.
- **Event Binding**: Kullanıcı etkileşimlerini (örneğin, tıklama veya klavye girişi) bileşenin işlevlerine bağlar.

Angular, her iki tür bağlamayı birlikte kullanarak, kullanıcı etkileşimlerine dinamik ve doğru tepki verilmesini sağlar. Bu da kullanıcı etkileşimlerinin ve bileşenler arasındaki veri akışının yönetilmesini kolaylaştırır.

---
##  **Angular Routing** 

**Angular Routing**, tek sayfa uygulamaları (SPA) geliştirmek için kullanılan bir mekanizmadır ve uygulamanın farklı bölümleri arasında gezinti yapmayı sağlar. Bu özellik, kullanıcıların uygulamanın farklı sayfalarına geçiş yapabilmesini, sayfa yenilemesi olmadan içeriklerin dinamik olarak değiştirilmesini sağlar. Angular Routing, **URL değişikliklerini** takip eder ve uygun bileşeni render eder, bu sayede uygulama daha hızlı ve kullanıcı dostu hale gelir.

#### 1. **Routing Modülü ve Yapılandırması**

Angular Routing, **RouterModule** adı verilen bir modül ile sağlanır. Bu modül, yönlendirme işlemleri için gerekli yapılandırmaları içerir ve genellikle Angular uygulamalarının **AppModule** içinde import edilir. Uygulamanın yönlendirme yapılandırması, **Routes** dizisi içinde belirtilir.

```typescript
import { NgModule } from '@angular/core';
import { RouterModule, Routes } from '@angular/router';
import { HomeComponent } from './home/home.component';
import { AboutComponent } from './about/about.component';

const routes: Routes = [
  { path: '', component: HomeComponent },
  { path: 'about', component: AboutComponent }
];

@NgModule({
  imports: [RouterModule.forRoot(routes)],
  exports: [RouterModule]
})
export class AppRoutingModule { }
```

Burada, `RouterModule.forRoot(routes)` ile yönlendirme yapısının kök modüle dahil edilmesi sağlanır. **Routes** dizisi, her yönlendirme için bir **path** (yol) ve bu yola karşılık gelecek **component**'i tanımlar.

#### 2. **RouterLink ve Navigation**

Angular Routing ile gezinmek için **routerLink** direktifi kullanılır. Bu, HTML içinde bir link oluşturmak için kullanılır ve kullanıcı tıkladığında belirli bir bileşene yönlendirilmesini sağlar.

```html
<a routerLink="/about">About</a>
```

Bu, `/about` yoluna tıklama ile yönlendirme yapar ve ilgili **AboutComponent**'i ekrana getirir.

Ayrıca, **programatik yönlendirme** için Angular `Router` servisi kullanılır. `Router.navigate()` metodu, bileşenlerden programatik olarak başka bir bileşene yönlendirme yapılmasını sağlar.

```typescript
import { Router } from '@angular/router';

constructor(private router: Router) {}

navigateToAbout() {
  this.router.navigate(['/about']);
}
```

#### 3. **Active Route ve Styling**

Angular Routing, kullanıcının mevcut sayfa veya sekmesini izlemek için **routerLinkActive** direktifini sunar. Bu, kullanıcı belirli bir rota ile aktif olduğunda, o bağlantıya özel bir CSS sınıfı ekler.

```html
<a routerLink="/about" routerLinkActive="active">About</a>
```

Bu örnekte, eğer kullanıcı `/about` yolunda ise, bağlantıya **"active"** sınıfı eklenir. Bu özellik, aktif sayfa bağlantısını vurgulamak için yaygın olarak kullanılır.

#### 4. **Lazy Loading (Geç Yükleme)**

Angular'da **Lazy Loading**, yalnızca gerekli olduğunda belirli modüllerin yüklenmesini sağlar. Bu, uygulamanın başlangıç yükleme süresini hızlandırır ve sayfa geçişleri sırasında daha verimli bir deneyim sağlar. Lazy loading, **loadChildren** özelliği kullanılarak yapılandırılır.

```typescript
const routes: Routes = [
  { path: 'products', loadChildren: () => import('./products/products.module').then(m => m.ProductsModule) }
];
```

Burada, `ProductsModule` yalnızca kullanıcı `/products` yoluna geldiğinde yüklenir.

#### 5. **Route Guards (Yönlendirme Koruyucuları)**

Angular Routing, belirli sayfalara erişimi kısıtlamak için **Route Guards** kullanmanızı sağlar. Bu koruyucular, bir yönlendirmeye izin verilip verilmeyeceğini kontrol eder ve erişim denetimi sağlar. Örneğin, **canActivate** koruyucu, bir kullanıcı belirli bir sayfaya gitmeye çalıştığında, sayfaya erişmeden önce bir koşul kontrolü yapabilir.

```typescript
import { CanActivate } from '@angular/router';

@Injectable({
  providedIn: 'root'
})
export class AuthGuard implements CanActivate {

  constructor(private authService: AuthService) {}

  canActivate(): boolean {
    return this.authService.isAuthenticated();
  }
}
```

Bu örnekte, `AuthGuard` yalnızca kullanıcının **isAuthenticated** metodundan true döndürmesi durumunda rotaya erişime izin verir.

#### 6. **Nested Routes (İç İçe Yönlendirmeler)**

Angular Routing, bir rota içinde başka bir rota tanımlamak için iç içe yönlendirmelere (nested routes) olanak tanır. Bu özellik, uygulamanın bir kısmını başka bir kısmın içinde görüntülemek için kullanılır.

```typescript
const routes: Routes = [
  {
    path: 'dashboard',
    component: DashboardComponent,
    children: [
      { path: 'user', component: UserComponent },
      { path: 'settings', component: SettingsComponent }
    ]
  }
];
```

Burada, `/dashboard` yolu, **DashboardComponent**'i yükler ve bu bileşenin içinde **UserComponent** ve **SettingsComponent** bileşenleri yer alır.

#### 7. **404 Sayfası ve Yönlendirme**

Uygulamada tanımlı olmayan bir yola gidildiğinde, kullanıcıyı özel bir hata sayfasına yönlendirmek için `pathMatch: 'full'` ile bir yönlendirme yapılabilir. Bu genellikle **404 sayfası** için kullanılır.

```typescript
const routes: Routes = [
  { path: '**', component: PageNotFoundComponent }
];
```

Bu, mevcut olmayan bir yola gidildiğinde, `PageNotFoundComponent`'in görüntülenmesini sağlar.

---

## **Dependency Injection (DI)**

**Dependency Injection (DI)**, yazılım geliştirmede kullanılan bir tasarım desenidir ve Angular’da, bileşenler, servisler ve diğer sınıflar arasında bağımlılıkların yönetilmesini sağlar. DI, bir nesnenin ihtiyaç duyduğu bağımlılıkları dışarıdan almasını sağlayarak, yazılımın esnekliğini, test edilebilirliğini ve sürdürülebilirliğini artırır. Angular, DI'yi uygulamanın her yerinde otomatik olarak kullanır ve uygulamanın modüler yapısını güçlendirir.

#### 1. **Dependency Injection Temelleri**

Angular'da DI, bir bileşen ya da servis başka bir servisi veya bileşeni kullanmaya ihtiyaç duyduğunda, bu ihtiyaç dışarıdan **constructor** aracılığıyla sağlanır. Angular, bağımlılıkları çözmek için **Injector** adında bir mekanizma kullanır. Bir bileşen ya da servis, ihtiyacı olan sınıfın örneğini **constructor** üzerinden alır.

```typescript
import { Component } from '@angular/core';
import { DataService } from './data.service';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
export class AppComponent {
  constructor(private dataService: DataService) {}
}
```

Bu örnekte, **AppComponent**, **DataService** bağımlılığını **constructor** aracılığıyla alır. Bu, Angular’ın DI mekanizmasının bir örneğidir.

#### 2. **Provider'lar ve Injectable**

Angular'da bağımlılıkları çözmek için **@Injectable** dekoratörü kullanılır. Bir sınıfın DI konteyneri tarafından kullanılabilmesi için, bu sınıfın bir **provider** olarak tanımlanması gerekir. **@Injectable** dekoratörü, sınıfın constructor'ında başka bir servisi almasına olanak tanır.

```typescript
import { Injectable } from '@angular/core';

@Injectable({
  providedIn: 'root'
})
export class DataService {
  getData() {
    return ['Data 1', 'Data 2', 'Data 3'];
  }
}
```

Bu örnekte, **DataService** sınıfı, **providedIn: 'root'** ile uygulama genelinde kullanılmak üzere bir provider olarak tanımlanmıştır. Bu, Angular’ın DI konteynerine **DataService**’i dahil eder ve her yerden erişilebilir kılar.

#### 3. **Bağımlılıkların Yaşam Süresi**

Angular, **@Injectable** dekoratörü ile sağlanan bağımlılıkların yaşam süresini yönetir. DI sistemi, sınıfın bir örneğini oluşturduğunda, bu örneğin yaşam süresi **provider** tanımına göre belirlenir. Yaygın yaşam süreleri şunlardır:

- **Singleton**: Uygulama boyunca tek bir örnek oluşturulur. Bu, Angular’ın default davranışıdır. `providedIn: 'root'` kullanarak bir sınıf global olarak singleton olarak sağlanabilir.
  
- **Scoped (Modül bazında)**: Eğer bağımlılık sadece bir modül içinde geçerli olacaksa, `providedIn: 'any'` veya modül düzeyinde provider tanımlanabilir.

- **Per Component**: Her bileşen için yeni bir bağımlılık örneği oluşturulabilir. Bunun için provider, bileşen seviyesinde tanımlanır.

```typescript
@Component({
  selector: 'app-example',
  templateUrl: './example.component.html',
  styleUrls: ['./example.component.css'],
  providers: [DataService]  // Yalnızca bu bileşen için DataService örneği sağlanır
})
export class ExampleComponent {
  constructor(private dataService: DataService) {}
}
```

#### 4. **DI’nin Avantajları**

- **Modülerlik ve Yeniden Kullanılabilirlik**: DI, bileşenler ve servisler arasında güçlü bir gevşek bağ sağlar. Bu sayede, bir bileşen yalnızca ihtiyacı olan servisi alır ve başka bileşenlere bağımlı olmaz. Bu, yazılımın modülerliğini artırır.

- **Test Edilebilirlik**: DI, bağımlılıkların dışarıdan enjekte edilmesi sayesinde birimler arası bağımlılıkları en aza indirir. Bu, birimleri bağımsız olarak test etmeyi kolaylaştırır. Testler sırasında gerçek servisler yerine **mock** servisler kullanarak test yapılabilir.

- **Bakım Kolaylığı**: Bağımlılıklar dışarıdan enjekte edildiği için, kodun bakımını yapmak daha kolaydır. Bağımlılıkların değişmesi gerektiğinde, yalnızca DI yapılandırması değiştirilir; servislerin kendisinde değişiklik yapılması gerekmez.

#### 5. **Hierarchical Dependency Injection (Hiyerarşik DI)**

Angular’ın DI sistemi, hiyerarşik bir yapıya sahiptir. Bu, DI konteynerlerinin, daha küçük alt konteynerler tarafından yönetildiği anlamına gelir. Uygulama, modüller ve bileşenler arasında farklı DI konteynerlerine sahip olabilir. Örneğin, bir servisin kök modülde bir örneği oluşturulabilirken, belirli bir bileşen içinde yeniden oluşturulabilir.

Bu, özellikle büyük uygulamalarda, her modül veya bileşenin kendi bağımlılıklarını yönetmesini sağlayarak esneklik ve performans artışı sağlar.

#### 6. **Factory Providers ve useClass / useValue / useFactory**

Angular, bağımlılıkları enjekte ederken yalnızca sınıf örnekleri değil, aynı zamanda **value**, **factory** veya **class** kullanarak da sağlayabilir. Bu, daha dinamik ve özelleştirilmiş bağımlılıkları yönetmeye olanak tanır.

- **useClass**: Belirtilen sınıfı kullanarak bağımlılığı enjekte eder.
  
- **useValue**: Sabit bir değer sağlar.

- **useFactory**: Bir fabrika fonksiyonu kullanarak bağımlılığı sağlar.

```typescript
@NgModule({
  providers: [
    {
      provide: DataService,
      useClass: MockDataService  // Mock veriyi kullanmak için
    }
  ]
})
export class AppModule { }
```

Burada, **DataService** yerine **MockDataService** sınıfı sağlanır.

#### 7. **Angular DI'nin Özet Faydaları**

- **Bağımlılıkların yönetimi basitleştirilir**.
- **Yazılımın modülerliği artırılır**, böylece daha esnek ve sürdürülebilir bir uygulama elde edilir.
- **Test süreçleri kolaylaşır**, çünkü bağımlılıklar dışarıdan enjekte edilir ve mock'lar kullanılabilir.
- **Performans optimizasyonu** yapılabilir, çünkü bağımlılıklar yalnızca gerekli olduğunda yüklenir.
  
**Özetle**, **Dependency Injection (DI)**, Angular’da kodun daha sürdürülebilir, test edilebilir ve esnek olmasını sağlayan bir mekanizmadır. Bağımlılıklar dışarıdan enjekte edilerek, uygulamanın bileşenleri arasındaki bağımlılıklar minimuma indirilir ve bakım ile test süreçleri kolaylaştırılır. Bu özellik, Angular’ın güçlü modüler yapısını destekler ve büyük uygulamalarda performans ve yönetilebilirlik avantajları sağlar.

---

## **Forms**

Angular’da **Forms**, kullanıcı girdilerini işlemek, doğrulamak ve bu girdileri model verileriyle senkronize etmek için kullanılan güçlü bir yapıdır. Angular, iki tür form yönetimi yaklaşımı sunar: **Template-Driven Forms** ve **Reactive Forms**. Her iki yaklaşım da farklı ihtiyaçlara göre özelleştirilebilir ve birlikte kullanılabilir.


#### 1. **Template-Driven Forms**

Template-Driven Forms, HTML şablonlarında form işlevselliğini tanımlamaya odaklanır ve Angular'ın form altyapısını kullanarak iki yönlü veri bağlama (**two-way binding**) ile çalışır. Daha küçük ve basit formlar için idealdir.

**Örnek Kullanım:**
```html
<form #form="ngForm" (ngSubmit)="onSubmit(form)">
  <input type="text" name="name" ngModel required />
  <button type="submit">Submit</button>
</form>
```

- **ngModel**: Veri bağlama için kullanılır.
- **#form="ngForm"**: Angular’ın form kontrol referansını şablona bağlar.
- **required**: Angular’ın yerleşik doğrulama mekanizmalarından biridir.

**Avantajları:**
- Basit ve hızlıdır.
- Küçük projeler ve temel formlar için uygundur.

**Dezavantajları:**
- Büyük ve karmaşık formlarda kod yönetimi zorlaşabilir.
- Daha az kontrol ve özelleştirme sunar.

#### 2. **Reactive Forms**

Reactive Forms, form durumunu ve doğrulamayı tamamen TypeScript tarafında tanımlar. Bu, form mantığının daha kolay test edilmesini ve yönetilmesini sağlar. Karmaşık ve dinamik formlar için uygundur.

**Örnek Kullanım:**
```typescript
import { Component } from '@angular/core';
import { FormGroup, FormControl, Validators } from '@angular/forms';

@Component({
  selector: 'app-reactive-form',
  template: `
    <form [formGroup]="form" (ngSubmit)="onSubmit()">
      <input formControlName="name" />
      <button type="submit">Submit</button>
    </form>
  `
})
export class ReactiveFormComponent {
  form = new FormGroup({
    name: new FormControl('', Validators.required)
  });

  onSubmit() {
    console.log(this.form.value);
  }
}
```

- **FormGroup**: Bir formun mantıksal grubu.
- **FormControl**: Form alanlarını temsil eder.
- **Validators**: Doğrulama kuralları tanımlamak için kullanılır.

**Avantajları:**
- Daha güçlü doğrulama ve durum yönetimi.
- Dinamik form alanlarının oluşturulması kolaydır.
- Test edilebilirlik ve kontrol açısından daha esnektir.

**Dezavantajları:**
- Daha fazla kod yazmayı gerektirir.
- İlk öğrenme eğrisi daha yüksektir.


#### 3. **Doğrulama**

Angular formlarında doğrulama kuralları, hem yerleşik validator’lar hem de özel validator’lar aracılığıyla uygulanabilir.

**Yerleşik Validator’lar:**
- **required**: Alanın doldurulmasını zorunlu kılar.
- **minlength** ve **maxlength**: Minimum ve maksimum karakter uzunlukları.
- **pattern**: Regex doğrulaması.

**Özel Validator’lar:**
```typescript
import { AbstractControl, ValidationErrors } from '@angular/forms';

export function customValidator(control: AbstractControl): ValidationErrors | null {
  return control.value.includes('Angular') ? null : { invalidWord: true };
}
```
#### 4. **Form Durumları**

Angular, formların ve form alanlarının durumunu izler:
- **Pristine/Dirty**: Alanın değiştirilip değiştirilmediğini belirtir.
- **Touched/Untouched**: Kullanıcının alana odaklanıp odaklanmadığını belirtir.
- **Valid/Invalid**: Alanın doğrulama kurallarına uyup uymadığını belirtir.

Bu durumlar, kullanıcıya geri bildirim sağlamak için kullanılabilir:
```html
<input formControlName="name" />
<div *ngIf="form.get('name')?.invalid && form.get('name')?.touched">
  Name is required.
</div>
```

#### 5. **Dinamik Formlar**

Angular Reactive Forms, dinamik olarak form alanları eklemek veya kaldırmak için uygundur.

**Örnek:**
```typescript
addControl() {
  this.form.addControl('newField', new FormControl('', Validators.required));
}
```

#### 6. **Formların İletilmesi ve Veri Bağlama**

Hem Template-Driven Forms hem de Reactive Forms, kullanıcı girdilerini model verileriyle bağlamak için veri bağlama (data binding) kullanır. Reactive Forms’da, `form.value` ile tüm form verilerine kolayca erişilebilir.


#### 7. **FormsModule ve ReactiveFormsModule**

Formlarla çalışmak için Angular’da iki temel modül vardır:
- **FormsModule**: Template-Driven Forms için gereklidir.
- **ReactiveFormsModule**: Reactive Forms için gereklidir.

Bu modüller, **AppModule** ya da ilgili bir modülde içe aktarılmalıdır.

**Örnek:**
```typescript
import { FormsModule, ReactiveFormsModule } from '@angular/forms';

@NgModule({
  imports: [FormsModule, ReactiveFormsModule],
})
export class AppModule {}
```


#### 8. **Hangi Yaklaşım Ne Zaman Kullanılır?**

- **Template-Driven Forms**: Basit, statik formlar için uygun.
- **Reactive Forms**: Karmaşık doğrulamalar, dinamik alanlar ve daha güçlü kontrol gereken durumlar için idealdir.


**Sonuç:** Angular Forms sistemi, kullanıcı girdilerini işlemek ve doğrulamak için hem basit hem de karmaşık çözümler sunar. Template-Driven Forms, daha temel ve hızlı uygulamalar için uygundur. Reactive Forms ise esneklik ve test edilebilirlik açısından daha güçlüdür ve büyük projelerde önerilir.

---

## **Services ve HTTP Istekleri**

Angular’da **Services**, uygulama mantığını bileşenlerden ayırmak ve kodun yeniden kullanılabilirliğini sağlamak için kullanılan sınıflardır. Uygulama genelinde verileri paylaşmak, iş mantığını merkezi bir şekilde yönetmek ve dış API'larla iletişim kurmak için hizmetler kullanılır.

#### **Service Tanımı ve Kullanımı**
Angular'da bir service, genellikle **@Injectable** dekoratörü ile tanımlanır ve DI (Dependency Injection) aracılığıyla bileşenlere enjekte edilir.

**Örnek Service:**
```typescript
import { Injectable } from '@angular/core';

@Injectable({
  providedIn: 'root', // Hizmet, tüm uygulama genelinde kullanılabilir.
})
export class DataService {
  getData() {
    return ['Angular', 'React', 'Vue'];
  }
}
```

Bu servisi bir bileşende kullanmak için DI mekanizması kullanılır:
```typescript
import { Component } from '@angular/core';
import { DataService } from './data.service';

@Component({
  selector: 'app-root',
  template: `<ul><li *ngFor="let item of data">{{ item }}</li></ul>`,
})
export class AppComponent {
  data: string[];

  constructor(private dataService: DataService) {
    this.data = this.dataService.getData();
  }
}
```

#### **HTTP İstekleri**
Angular, HTTP isteklerini gerçekleştirmek için **HttpClient** modülünü sağlar. Bu modül, RESTful API'larla iletişim kurmayı kolaylaştırır ve HTTP yöntemlerini (GET, POST, PUT, DELETE vb.) destekler.

**HttpClient Modülü Kullanımı:**
HttpClient, **HttpClientModule**'ün **AppModule**'e eklenmesiyle kullanılır:
```typescript
import { HttpClientModule } from '@angular/common/http';

@NgModule({
  imports: [HttpClientModule],
})
export class AppModule {}
```

**GET İsteği:**
```typescript
import { HttpClient } from '@angular/common/http';
import { Injectable } from '@angular/core';

@Injectable({
  providedIn: 'root',
})
export class ApiService {
  constructor(private http: HttpClient) {}

  fetchData() {
    return this.http.get('https://jsonplaceholder.typicode.com/posts');
  }
}
```

Bu verileri bir bileşende kullanmak için:
```typescript
import { Component } from '@angular/core';
import { ApiService } from './api.service';

@Component({
  selector: 'app-root',
  template: `<ul><li *ngFor="let post of posts">{{ post.title }}</li></ul>`,
})
export class AppComponent {
  posts: any[] = [];

  constructor(private apiService: ApiService) {
    this.apiService.fetchData().subscribe((data: any) => {
      this.posts = data;
    });
  }
}
```

#### **HTTP İsteklerinde Error Handling**
HTTP istekleri sırasında hata yönetimi önemlidir. Angular'da **catchError** operatörü kullanılarak hatalar yakalanabilir:
```typescript
import { catchError } from 'rxjs/operators';
import { throwError } from 'rxjs';

fetchData() {
  return this.http.get('https://jsonplaceholder.typicode.com/posts').pipe(
    catchError((error) => {
      console.error('Error:', error);
      return throwError(() => new Error('Bir hata oluştu!'));
    })
  );
}
```

#### **Interceptor Kullanımı**
Tüm HTTP isteklerini merkezi bir şekilde yönetmek için **HTTP Interceptor** kullanılabilir. Bu, token ekleme, hata yönetimi veya logging gibi işlemler için idealdir.

**Interceptor Tanımı:**
```typescript
import { Injectable } from '@angular/core';
import { HttpInterceptor, HttpRequest, HttpHandler } from '@angular/common/http';

@Injectable()
export class AuthInterceptor implements HttpInterceptor {
  intercept(req: HttpRequest<any>, next: HttpHandler) {
    const clonedRequest = req.clone({
      headers: req.headers.set('Authorization', 'Bearer token'),
    });
    return next.handle(clonedRequest);
  }
}
```

**AppModule'e Eklenmesi:**
```typescript
import { HTTP_INTERCEPTORS } from '@angular/common/http';

@NgModule({
  providers: [
    { provide: HTTP_INTERCEPTORS, useClass: AuthInterceptor, multi: true },
  ],
})
export class AppModule {}
```

#### **HTTP İsteklerinde Observable ve Promise Kullanımı**
- Angular'da HTTP istekleri genellikle **Observable** üzerinden yapılır ve **RxJS** operatörleriyle yönetilir.
- İstekleri **Promise**'a dönüştürmek gerekiyorsa:
```typescript
this.http.get('url').toPromise().then((data) => console.log(data));
```

#### **Özet**
- **Services**, uygulama mantığını merkezi bir yerde toplar ve kodun yeniden kullanılabilirliğini artırır.
- **HttpClient**, RESTful API'larla iletişim kurmayı kolaylaştırır ve Angular'da HTTP isteklerinin temelini oluşturur.
- Hata yönetimi ve interceptors, güvenli ve düzenli HTTP işlemleri için kritik öneme sahiptir.

---

## **Pipes**

**Pipes**, Angular'da verilerin kullanıcıya gösterilmeden önce dönüştürülmesini veya formatlanmasını sağlayan araçlardır. Template'lerde veriyi kolayca biçimlendirmek için kullanılır.

#### **Angular'da Hazır Pipes**
Angular, sık kullanılan işlemler için hazır gelen birçok pipe sunar:

1. **DatePipe**: Tarihleri formatlamak için kullanılır.
   ```html
   <p>{{ today | date:'fullDate' }}</p>
   ```
   - `short`, `medium`, `long`, `full` gibi formatlar kullanılabilir.

2. **CurrencyPipe**: Sayıları para birimine dönüştürmek için kullanılır.
   ```html
   <p>{{ amount | currency:'USD' }}</p>
   ```

3. **UpperCasePipe ve LowerCasePipe**: Metinleri büyük/küçük harfe çevirmek için kullanılır.
   ```html
   <p>{{ message | uppercase }}</p>
   <p>{{ message | lowercase }}</p>
   ```

4. **DecimalPipe**: Sayıları ondalık basamaklarla biçimlendirmek için kullanılır.
   ```html
   <p>{{ 1234.567 | number:'1.2-2' }}</p>
   ```

5. **PercentPipe**: Yüzde formatında göstermek için kullanılır.
   ```html
   <p>{{ ratio | percent }}</p>
   ```

6. **SlicePipe**: Bir diziyi veya metni belirli aralıklarda kesmek için kullanılır.
   ```html
   <p>{{ names | slice:0:2 }}</p>
   ```

7. **JsonPipe**: Nesneleri JSON formatında göstermek için kullanılır.
   ```html
   <pre>{{ data | json }}</pre>
   ```

#### **Custom Pipes**
Angular, özel ihtiyaçlar için kendi pipe'larınızı oluşturmanıza olanak tanır.

**Özel Pipe Tanımı:**
```typescript
import { Pipe, PipeTransform } from '@angular/core';

@Pipe({
  name: 'reverse'
})
export class ReversePipe implements PipeTransform {
  transform(value: string): string {
    return value.split('').reverse().join('');
  }
}
```

**Kullanımı:**
```html
<p>{{ 'Angular' | reverse }}</p> <!-- Çıktı: ralugnA -->
```

#### **Pure ve Impure Pipes**
- **Pure Pipes**: Girdi değiştiğinde yeniden çalışır. Varsayılan olarak tüm pipe'lar pure'dir.
- **Impure Pipes**: Her değişiklikte çalışır ve performansı olumsuz etkileyebilir. `pure: false` olarak ayarlanır.

**Impure Pipe Tanımı:**
```typescript
@Pipe({
  name: 'filter',
  pure: false
})
export class FilterPipe implements PipeTransform {
  transform(items: any[], searchTerm: string): any[] {
    return items.filter(item => item.includes(searchTerm));
  }
}
```

---

##  **Directives**

Directives, Angular'da DOM ile doğrudan çalışarak davranışları değiştiren yapılardır. Üç temel türü vardır:
1. **Structural Directives**: DOM'u manipüle eder.
2. **Attribute Directives**: Bir elementin görünümünü veya davranışını değiştirir.
3. **Custom Directives**: Özel ihtiyaçlar için oluşturulan direktiflerdir.

#### **Structural Directives**
- DOM'u ekleme veya çıkarma işlemlerini gerçekleştirir.
- Örnekler:
  - **`*ngIf`**: Bir elementi koşula bağlı olarak gösterir veya gizler.
    ```html
    <p *ngIf="isVisible">Bu metin görünür.</p>
    ```

  - **`*ngFor`**: Bir listeyi döngüyle işler.
    ```html
    <ul>
      <li *ngFor="let item of items">{{ item }}</li>
    </ul>
    ```

  - **`*ngSwitch`**: Koşullu dallanmalar için kullanılır.
    ```html
    <div [ngSwitch]="status">
      <p *ngSwitchCase="'active'">Aktif</p>
      <p *ngSwitchCase="'inactive'">Pasif</p>
      <p *ngSwitchDefault>Durum bilinmiyor</p>
    </div>
    ```

#### **Attribute Directives**
- Bir elementin görünümünü veya davranışını değiştirir.
- Örnek: **`ngClass` ve `ngStyle`**
  ```html
  <p [ngClass]="{'highlight': isActive}">Stil uygulanmış metin</p>
  <p [ngStyle]="{'color': 'blue'}">Renkli metin</p>
  ```

#### **Custom Directives**
Özel bir direktif, Angular’da bir sınıf olarak tanımlanır ve `@Directive` dekoratörü ile işaretlenir.

**Özel Direktif Örneği:**
```typescript
import { Directive, ElementRef, Renderer2, HostListener } from '@angular/core';

@Directive({
  selector: '[appHighlight]'
})
export class HighlightDirective {
  constructor(private el: ElementRef, private renderer: Renderer2) {}

  @HostListener('mouseenter') onMouseEnter() {
    this.renderer.setStyle(this.el.nativeElement, 'backgroundColor', 'yellow');
  }

  @HostListener('mouseleave') onMouseLeave() {
    this.renderer.removeStyle(this.el.nativeElement, 'backgroundColor');
  }
}
```

**Kullanımı:**
```html
<p appHighlight>Üzerine geldiğinizde vurgulanan metin</p>
```

---

## **Angular CLI (Command Line Interface)**

Angular CLI, Angular projelerini hızlı ve verimli bir şekilde oluşturmak, geliştirmek ve yönetmek için kullanılan bir araçtır. Angular CLI, uygulamaların yapısını otomatikleştirir ve karmaşıklığı azaltır.

#### **Angular CLI Kurulumu**
```bash
npm install -g @angular/cli
```

#### **Önemli Komutlar**
1. **Yeni Proje Oluşturma**
   ```bash
   ng new proje-adi
   ```

2. **Bir Bileşen Oluşturma**
   ```bash
   ng generate component bileşen-adı
   ```

3. **Bir Hizmet Oluşturma**
   ```bash
   ng generate service hizmet-adı
   ```

4. **Projeyi Çalıştırma**
   ```bash
   ng serve
   ```

5. **Build İşlemi**
   ```bash
   ng build --prod
   ```

6. **Test Çalıştırma**
   ```bash
   ng test
   ```

#### **CLI ile Yapılandırma**
- **Angular.json** dosyası ile proje ayarları yapılır.
- CLI'nın özelleştirilmesi mümkündür.

---

Evet, 10. madde eksik kaldı ve daha kapsamlı bir açıklama yapmam gerekirdi. İşte daha detaylı bir anlatım:  

---

## **State Management**

State management, bir uygulama içindeki verilerin tutarlı bir şekilde yönetilmesini sağlar. Angular gibi modern web uygulamalarında, farklı bileşenler ve servisler arasında veri paylaşımı ve senkronizasyon karmaşık hale gelebilir. Bu karmaşıklığı yönetmek için state management stratejileri ve araçları kullanılır.  

#### **State Management Türleri**  
1. **Component State**  
   - Her bileşenin kendi içinde tutulan durumu ifade eder.  
   - Küçük ölçekli uygulamalarda yeterli olabilir.  
   - Örnek: Form verilerinin bir bileşende tutulması.  
   ```typescript
   export class MyComponent {
     myData = 'Hello Angular';
   }
   ```

2. **Global State**  
   - Tüm uygulama genelinde erişilebilen ve yönetilebilen durumdur.  
   - Karmaşık uygulamalarda veri senkronizasyonunu kolaylaştırır.  
   - Örnek: Kullanıcı oturum bilgileri veya alışveriş sepeti durumu.  

#### **State Management Araçları**  
Angular'da state management için çeşitli yöntemler ve araçlar kullanılabilir:  

1. **RxJS (Reactive Extensions for JavaScript)**  
   - Angular'ın reaktif programlama kütüphanesi olan RxJS, state yönetimi için güçlü bir araçtır.  
   - Observable ve Subject kullanarak bileşenler arasında veri paylaşımı yapılabilir.  
   ```typescript
   import { BehaviorSubject } from 'rxjs';

   export class StateService {
     private state = new BehaviorSubject<number>(0);
     currentState = this.state.asObservable();

     updateState(newState: number) {
       this.state.next(newState);
     }
   }
   ```

2. **NgRx (Redux Tarzı Yaklaşım)**  
   - Angular için popüler bir state management kütüphanesidir.  
   - Redux prensiplerine dayanır: tek bir global state, değişmezlik ve aksiyonlar.  
   - Anahtar bileşenler: **Store**, **Actions**, **Reducers**, **Selectors**, **Effects**.  

   **NgRx Kullanımı:**
   ```bash
   npm install @ngrx/store @ngrx/effects
   ```

   Örnek bir reducer:  
   ```typescript
   import { createReducer, on } from '@ngrx/store';
   import { increment, decrement } from './counter.actions';

   export const initialState = 0;

   const _counterReducer = createReducer(
     initialState,
     on(increment, (state) => state + 1),
     on(decrement, (state) => state - 1)
   );

   export function counterReducer(state, action) {
     return _counterReducer(state, action);
   }
   ```

3. **Akita**  
   - Daha az karmaşık bir alternatif olarak kullanılabilir.  
   - Store, Query, ve Service tabanlı bir yaklaşıma sahiptir.  

4. **Service-based State Management**  
   - Angular servislerini kullanarak manuel state yönetimi yapılabilir.  
   - Basit uygulamalar için uygundur.  
   ```typescript
   export class AppStateService {
     private _state = new BehaviorSubject<any>({});
     state$ = this._state.asObservable();

     setState(newState: any) {
       this._state.next(newState);
     }
   }
   ```

#### **State Management için En İyi Uygulamalar**  
1. **Tek Kaynak Prensibi (Single Source of Truth):** Tüm veriler bir yerde tutulmalı ve oradan yönetilmelidir.  
2. **State Normalization:** State nesnesi sade ve ilişkilendirilebilir bir yapıda olmalıdır.  
3. **Immutable Data:** State değişiklikleri yapılırken eski değer değiştirilmemeli, yeni bir kopya oluşturulmalıdır.  
4. **Selectors Kullanımı:** Gereksiz işlem yükünden kaçınmak için state'e erişim optimize edilmelidir.  

#### **State Yönetiminin Avantajları**  
- Veri tutarlılığını artırır.  
- Kodun okunabilirliğini ve bakımını kolaylaştırır.  
- Karmaşık uygulamalarda bileşenler arasında veri paylaşımını basitleştirir.  

---  

## **Testing**

Angular projelerinde testler, uygulamanın güvenilirliğini ve sürdürülebilirliğini sağlamak için kritik bir rol oynar. Angular, test yazımı için zengin bir altyapı sunar ve iki temel test türü vardır: **Unit Test** ve **End-to-End (E2E) Test**.

#### **Unit Test**
- **Amaç:** Tek birimlerin (bileşen, servis, pipe gibi) doğru çalıştığını kontrol etmek.  
- Angular CLI, test altyapısını otomatik olarak sağlar.  
- **Jasmine ve Karma** en yaygın kullanılan araçlardır.  

**Birim Test Örneği:**  
Bir bileşenin başlığını kontrol eden test:  
```typescript
import { ComponentFixture, TestBed } from '@angular/core/testing';
import { MyComponent } from './my.component';

describe('MyComponent', () => {
  let component: MyComponent;
  let fixture: ComponentFixture<MyComponent>;

  beforeEach(async () => {
    await TestBed.configureTestingModule({
      declarations: [MyComponent],
    }).compileComponents();

    fixture = TestBed.createComponent(MyComponent);
    component = fixture.componentInstance;
    fixture.detectChanges();
  });

  it('should have a title', () => {
    expect(component.title).toBe('My App');
  });
});
```

#### **E2E Test**
- **Amaç:** Uygulamanın tüm bileşenlerinin birlikte doğru çalıştığını kontrol etmek.  
- Angular CLI, E2E testleri için **Protractor** entegrasyonu sağlar (ancak Cypress gibi modern araçlar daha sık tercih edilmektedir).  

**E2E Test Örneği:**  
Bir butonun tıklanabilirliğini kontrol eden test:  
```typescript
describe('App', () => {
  it('should navigate to the home page', () => {
    cy.visit('/');
    cy.contains('Home').click();
    cy.url().should('include', '/home');
  });
});
```

#### **Testler için En İyi Uygulamalar**
1. **Test Küçük Başlatılmalı:** Her bileşen veya servis için küçük ve izole testler yazın.  
2. **Mock ve Stub Kullanımı:** Servis ve veri bağımlılıklarını izole etmek için sahte veri sağlayıcılar kullanın.  
3. **Kod Kapsamını Ölçün:** Testlerin kodun ne kadarını kapsadığını belirlemek için araçlar (ör. Istanbul) kullanın.  

---

## **Performance Optimization**

Performans optimizasyonu, kullanıcı deneyimini iyileştirmek ve uygulamanın hızlı çalışmasını sağlamak için önemlidir. Angular’da performansı artırmak için kullanılabilecek birçok teknik vardır.

#### **Performans Optimizasyonu Teknikleri**
1. **Lazy Loading:** Modüllerin yalnızca ihtiyaç duyulduğunda yüklenmesi.
   ```typescript
   const routes: Routes = [
     { path: 'dashboard', loadChildren: () => import('./dashboard/dashboard.module').then(m => m.DashboardModule) }
   ];
   ```

2. **Change Detection Optimizasyonu:**  
   - **OnPush Strategy** kullanarak gereksiz değişiklik algılamalarını önleyin.  
   ```typescript
   @Component({
     changeDetection: ChangeDetectionStrategy.OnPush,
   })
   ```

3. **TrackBy Kullanımı (ngFor):**  
   - Angular'ın liste elemanlarını daha hızlı güncellemesi için kullanılır.  
   ```html
   <div *ngFor="let item of items; trackBy: trackByFn">{{ item.name }}</div>
   ```

4. **Preloading Strategies:** Lazy loading yapılırken bile sayfaların önceden yüklenmesini sağlar.  
   ```typescript
   RouterModule.forRoot(routes, { preloadingStrategy: PreloadAllModules });
   ```

5. **Optimize Edilmiş Görüntüler ve Dosyalar:**  
   - Resim boyutlarını küçültmek ve gzip gibi sıkıştırma teknikleri kullanmak.  

#### **Performans Araçları**
- **Lighthouse:** Google’ın geliştirdiği, performans değerlendirme ve öneriler sunan araç.
- **Web.dev:** Performansı analiz edip iyileştirme önerileri sunar.

---

## **Internationalization (i18n) ve Localization (l10n)**

i18n ve l10n, uygulamanın farklı diller ve bölgelere göre uyarlanmasını sağlar.

#### **Internationalization (i18n)**
- Uygulamanın birden fazla dilde çalışmasını mümkün kılar.  
- Angular, yerleşik i18n modülüyle çeviri yönetimi sunar.

**Adımlar:**  
1. Çeviri etiketleri ekleyin:  
   ```html
   <h1 i18n="@@welcomeMessage">Welcome to My App</h1>
   ```

2. Çeviri dosyasını dışa aktarın:  
   ```bash
   ng extract-i18n
   ```

3. Çevirileri tamamlayın ve kullanın.  

#### **Localization (l10n)**
- Tarih, saat, para birimi gibi yerel öğelerin uyarlanmasını sağlar.  
- Angular’ın `DatePipe` ve `CurrencyPipe` gibi özellikleri bu uyarlamayı kolaylaştırır.  
   ```typescript
   {{ today | date:'fullDate':'':'fr' }}
   ```

#### **Entegrasyon Araçları**
- **ngx-translate:** Angular için yaygın kullanılan bir çeviri kütüphanesidir.
   ```typescript
   import { TranslateService } from '@ngx-translate/core';

   constructor(private translate: TranslateService) {
     this.translate.use('en');
   }
   ```

--- 

## **Security**

Angular uygulamalarında güvenlik, uygulamanın kötü niyetli saldırılara karşı korunmasını sağlar.

#### **En Yaygın Güvenlik Tehditleri**
1. **Cross-Site Scripting (XSS):**  
   - Kullanıcı girişlerini temizlemek ve Angular’ın DOM sanitization özelliğini kullanmak.  
   - Örnek: `innerHTML` kullanımına dikkat etmek.
     ```typescript
     <div [innerHTML]="trustedHtml"></div>
     ```

2. **Cross-Site Request Forgery (CSRF):**  
   - CSRF tokenlarıyla koruma sağlanır.  
   - Backend ile token doğrulama yapılmalıdır.

3. **SQL Injection:**  
   - Angular doğrudan SQL işlemleri yapmaz, ancak backend'deki veri girişi kontrol edilmelidir.

#### **Angular’da Güvenlik Mekanizmaları**
1. **Sanitization:** Angular, DOM manipülasyonlarını otomatik olarak temizler.  
2. **Content Security Policy (CSP):** Uygulama içeriğini güvenli hale getirir.  
3. **Route Guards:** Kullanıcıların yetkisiz sayfalara erişimini engeller.  
   ```typescript
   canActivate(route: ActivatedRouteSnapshot, state: RouterStateSnapshot): boolean {
     return this.authService.isLoggedIn();
   }
   ```

---  

## **Progressive Web App (PWA)**

Progressive Web App (PWA), web teknolojileriyle native mobil uygulama deneyimi sunmayı hedefler. Angular, PWA özelliklerini kolayca entegre etmek için Angular Service Worker modülünü kullanır.

#### **PWA Özellikleri**
- **Offline Çalışma:** Ağ bağlantısı olmadan uygulamayı kullanabilme.
- **Push Notifications:** Kullanıcılarla etkileşim kurmayı sağlar.
- **Hızlı Yükleme:** Service Worker sayesinde sayfalar önbellekten hızlıca yüklenir.
- **Ana Ekrana Ekleme:** Kullanıcılar, uygulamayı bir mobil uygulama gibi cihazlarına yükleyebilir.

#### **PWA Angular Entegrasyonu**
1. **PWA Modülünü Ekleyin:**
   ```bash
   ng add @angular/pwa
   ```
   Bu komut `ngsw-config.json` adlı bir yapılandırma dosyası oluşturur.

2. **Service Worker Yapılandırması:**
   - **ngsw-config.json** dosyasını düzenleyerek önbellekleme stratejilerini tanımlayın.
   ```json
   {
     "index": "/index.html",
     "assetGroups": [
       {
         "name": "app",
         "installMode": "prefetch",
         "resources": {
           "files": ["/favicon.ico", "/index.html"]
         }
       }
     ]
   }
   ```

3. **Build ve Test:**  
   Uygulamanın production build’ini yaparak PWA özelliklerini test edin.  
   ```bash
   ng build --prod
   ```

---

## **Angular Universal (SSR)**

Angular Universal, Angular uygulamalarında server-side rendering (SSR) özelliğini etkinleştirir. SSR, uygulama içeriğini sunucuda oluşturur ve tarayıcıya gönderir, böylece hızlı yükleme ve SEO uyumluluğu sağlar.

#### **SSR’nin Avantajları**
1. **SEO Uyumlu:** Tarayıcılar ve arama motorları için tam HTML içerik sunar.
2. **Daha Hızlı İlk Yükleme:** Sunucuda işlenen HTML, tarayıcıya hızlıca yüklenir.
3. **Düşük Performanslı Cihazlar için Uygun:** Kullanıcı cihazına daha az yük bindirir.

#### **Angular Universal Kurulumu**
1. **Universal Modülünü Ekleyin:**
   ```bash
   ng add @nguniversal/express-engine
   ```
   Bu komut, SSR için gerekli dosyaları oluşturur.

2. **Server Uygulamasını Çalıştırın:**
   ```bash
   npm run dev:ssr
   ```

3. **Sunucu Taraflı Çalışma:**  
   Angular uygulaması, sunucuda Express.js yardımıyla çalıştırılır.

---

## **Angular Material**

Angular Material, modern ve erişilebilir kullanıcı arayüzleri oluşturmak için bir UI bileşen kütüphanesidir. Google’ın Material Design standartlarını uygular.

#### **Angular Material’in Avantajları**
- **Hazır Bileşenler:** Button, Card, Dialog, Table gibi birçok UI bileşeni sağlar.
- **Responsive Tasarım:** Mobil uyumlu bileşenler içerir.
- **Kolay Tema Desteği:** Renk şemaları ve temalar hızlıca uygulanabilir.

#### **Angular Material Entegrasyonu**
1. **Material’i Projeye Ekleyin:**
   ```bash
   ng add @angular/material
   ```

2. **Tema Seçimi ve Çalışma:**
   Material temalarını global CSS dosyanıza dahil edin:
   ```css
   @import '~@angular/material/prebuilt-themes/indigo-pink.css';
   ```

3. **Bileşenlerin Kullanımı:**
   Material bileşenlerini uygulamak için modülleri içe aktarın:
   ```typescript
   import { MatButtonModule } from '@angular/material/button';
   import { MatCardModule } from '@angular/material/card';
   ```

   **Örnek Kullanım:**
   ```html
   <mat-card>
     <mat-card-title>My Card</mat-card-title>
     <mat-card-content>Card Content</mat-card-content>
     <button mat-button>Click Me</button>
   </mat-card>
   ```

---

## **Build ve Deployment**

Angular uygulamalarını üretime hazır hale getirmek ve dağıtmak için yapılandırma ve dağıtım süreçleri kritik öneme sahiptir.

#### **Build Süreci**
1. **Production Build:**
   Angular CLI ile production build işlemini gerçekleştirin:
   ```bash
   ng build --prod
   ```

2. **Optimize Edilmiş Çıktı:**
   Build sırasında kod küçültme (minification), önyükleme optimizasyonu (tree shaking) ve AOT (Ahead-of-Time Compilation) uygulanır.

#### **Deployment Süreci**
- **Static Hosting:** Build edilen dosyalar statik bir sunucuda barındırılabilir (ör. Netlify, Vercel).  
- **Web Sunucusu Kullanımı:** Nginx veya Apache ile yapılandırma yapılabilir.
- **Cloud Hizmetleri:** AWS, Azure veya Google Cloud gibi platformlarda dağıtım yapılabilir.

**Nginx Konfigürasyonu:**
```nginx
server {
  listen 80;
  server_name my-angular-app.com;
  root /path/to/dist;

  location / {
    index index.html;
    try_files $uri /index.html;
  }
}
```

---

## **Module Federation**

Module Federation, mikro ön uç (micro-frontend) mimarisi oluşturmak için kullanılan bir Webpack özelliğidir. Angular’da farklı uygulamaların modüllerini bir araya getirmeye olanak tanır.

#### **Avantajları**
- **Bağımsız Geliştirme:** Farklı ekipler, farklı modüller üzerinde bağımsız çalışabilir.
- **Dinamik Yükleme:** Modüller, yalnızca ihtiyaç duyulduğunda yüklenir.
- **Tekrar Kullanılabilirlik:** Modüller farklı projelerde kullanılabilir.

#### **Kurulum**
1. Webpack için `ModuleFederationPlugin` yapılandırması yapılır:
   ```javascript
   new ModuleFederationPlugin({
     name: 'app',
     remotes: {
       mfe1: 'mfe1@http://localhost:3000/remoteEntry.js',
     },
   });
   ```

2. Angular uygulamasını Webpack ile çalıştırın:
   ```bash
   ng add angular-architects/module-federation
   ```

#### **Örnek Kullanım**
Bir mikro ön uç modülünü ana uygulamaya dahil etmek:
```typescript
import('./remoteEntry.js').then(m => m.ModuleName);
```

---


## **Custom Decorators**

Angular’da dekoratörler, sınıflara, metodlara, özelliklere veya parametrelere meta veri eklemek için kullanılır. Angular’ın sunduğu `@Component`, `@Injectable`, `@Input` gibi standart dekoratörlerin yanında, özel ihtiyaçları karşılamak için özelleştirilmiş dekoratörler (custom decorators) tanımlanabilir.

#### **Özelleştirilmiş Dekoratörlerin Avantajları**
- Tekrar kullanılabilir kod parçaları oluşturma.
- Modüller, bileşenler veya servislerde davranışı merkezi olarak kontrol etme.
- Metod seviyesinde giriş ve hata kontrolü yapma.

#### **Custom Decorator Örneği**
1. **Bir Logger Decorator:**
   Belirli bir metodun çağrılmasını loglamak için bir dekoratör tanımlayalım:
   ```typescript
   function LogMethod(target: any, propertyKey: string, descriptor: PropertyDescriptor) {
     const originalMethod = descriptor.value;
     descriptor.value = function (...args: any[]) {
       console.log(`Calling ${propertyKey} with arguments:`, args);
       return originalMethod.apply(this, args);
     };
   }
   ```

2. **Kullanımı:**
   ```typescript
   class ExampleService {
     @LogMethod
     fetchData(id: number) {
       console.log(`Fetching data for ID: ${id}`);
     }
   }

   const service = new ExampleService();
   service.fetchData(42); // Konsol çıktısı: Calling fetchData with arguments: [42]
   ```

3. **Parametre Dekoratörü:**
   Bir metodun parametresi üzerinde işlem yapmak için:
   ```typescript
   function ValidateParam(target: any, propertyKey: string, parameterIndex: number) {
     console.log(`Parameter validation for ${propertyKey} at index ${parameterIndex}`);
   }

   class Example {
     myMethod(@ValidateParam name: string) {
       console.log(`Hello, ${name}`);
     }
   }
   ```

---

## **WebSockets**

Angular’da WebSockets, gerçek zamanlı iletişim gerektiren uygulamalarda kullanılır. Örneğin, canlı sohbet uygulamaları veya anlık bildirim sistemleri.

#### **WebSocket Avantajları**
- **Gerçek Zamanlı İletişim:** Veri değişiklikleri hemen kullanıcılara iletilir.
- **Bilateral İletişim:** Hem istemciden sunucuya hem de sunucudan istemciye mesaj gönderimi mümkündür.
- **Hafif Protokol:** HTTP’ye kıyasla daha az yük ile çalışır.

#### **Angular’da WebSocket Kullanımı**
1. **WebSocket Bağlantısı Kurma:**
   Angular uygulamasında WebSocket bağlantısı kurmak için genellikle `rxjs` ile çalışılır.
   ```typescript
   import { webSocket } from 'rxjs/webSocket';

   const socket = webSocket('ws://localhost:8080');

   socket.subscribe(
     message => console.log('Message received:', message),
     err => console.error('Error:', err),
     () => console.log('Connection closed')
   );

   socket.next({ type: 'ping' });
   ```

2. **WebSocket Servisi:**
   WebSocket’i daha modüler hale getirmek için bir servis oluşturun:
   ```typescript
   import { Injectable } from '@angular/core';
   import { webSocket, WebSocketSubject } from 'rxjs/webSocket';

   @Injectable({
     providedIn: 'root'
   })
   export class WebSocketService {
     private socket$: WebSocketSubject<any> = webSocket('ws://localhost:8080');

     sendMessage(msg: any) {
       this.socket$.next(msg);
     }

     getMessages() {
       return this.socket$.asObservable();
     }
   }
   ```

---

## **Code Splitting**

Code Splitting (kod parçalama), Angular uygulamalarının boyutunu küçültmek ve başlangıç yükleme süresini optimize etmek için kullanılan bir tekniktir. Angular, bunu varsayılan olarak route-based lazy loading ile destekler.

#### **Avantajları**
- **Daha Hızlı İlk Yükleme:** Gereksiz kodların yüklenmesini engeller.
- **Dinamik Modüller:** Kullanıcı ihtiyaçlarına göre yükleme yapılır.
- **Performans Artışı:** Ağ ve bellek kaynaklarını verimli kullanır.

#### **Route-Based Lazy Loading**
1. **Modül Oluşturma:**
   Bir modülü lazy load edilecek şekilde yapılandırın:
   ```bash
   ng generate module feature --route feature --module app.module
   ```

2. **App Routing Yapılandırması:**
   ```typescript
   const routes: Routes = [
     { path: 'feature', loadChildren: () => import('./feature/feature.module').then(m => m.FeatureModule) }
   ];
   ```

3. **Dinamik Yükleme:**  
   Uygulama `feature` rotasına eriştiğinde, Angular yalnızca ilgili modülü yükler.

#### **Dinamik Komponent Yükleme**
Komponentleri runtime sırasında yüklemek için `ComponentFactoryResolver` kullanılabilir:
   ```typescript
   import { Component, ComponentFactoryResolver, ViewChild, ViewContainerRef } from '@angular/core';

   @Component({
     selector: 'app-dynamic',
     template: '<ng-container #container></ng-container>'
   })
   export class DynamicComponent {
     @ViewChild('container', { read: ViewContainerRef, static: true }) container: ViewContainerRef;

     constructor(private resolver: ComponentFactoryResolver) {}

     loadComponent(component: any) {
       const factory = this.resolver.resolveComponentFactory(component);
       this.container.createComponent(factory);
     }
   }
   ```

---

## **Service Worker Caching**

Angular Service Worker, uygulamaların performansını artırmak için cache yönetimini kolaylaştırır. Ayrıca, PWA geliştirme için temel bileşenlerden biridir.

#### **Service Worker’in Avantajları**
- **Offline Erişim:** Kullanıcılar, çevrimdışıyken bile uygulamayı kullanabilir.
- **Cache Yönetimi:** Sık kullanılan kaynakları önbelleğe alır.
- **Performans Artışı:** Ağa ihtiyaç duymadan içerik sunar.

#### **Angular’da Service Worker Kullanımı**
1. **Service Worker Eklemek:**
   ```bash
   ng add @angular/pwa
   ```

2. **ngsw-config.json Yapılandırması:**
   Cache politikalarını tanımlayın:
   ```json
   {
     "index": "/index.html",
     "assetGroups": [
       {
         "name": "app",
         "installMode": "prefetch",
         "resources": {
           "files": ["/favicon.ico", "/index.html", "/*.css", "/*.js"]
         }
       }
     ]
   }
   ```

3. **Uygulamayı Test Etmek:**  
   Service Worker’in çalıştığını kontrol etmek için uygulamayı bir HTTP sunucusunda çalıştırın:
   ```bash
   npx http-server ./dist/my-app
   ```
---
## **Web Components**

Web Components, modern web uygulamalarında, framework bağımsız, yeniden kullanılabilir ve kapsüllenmiş bileşenler oluşturmayı sağlayan bir teknolojidir. Angular, Web Components ile uyumlu bir şekilde çalışabilir.

#### **Web Components Temel Özellikleri**
1. **Shadow DOM:** Bileşenin stil ve yapısını kapsüller, dış dünyadan izole eder.
2. **Custom Elements:** Özel HTML etiketleri oluşturur.
3. **HTML Templates:** HTML şablonları ve içeriğini tekrar kullanılabilir hale getirir.

#### **Angular’da Web Components Kullanımı**
1. **Bileşeni Web Component’e Çevirme:**
   Angular’da bir bileşeni Web Component’e çevirmek için `@angular/elements` paketi kullanılır.
   ```bash
   ng add @angular/elements
   npm install --save-dev @webcomponents/custom-elements
   ```

2. **Web Component Tanımlama:**
   Angular bileşenini Web Component olarak kaydedin:
   ```typescript
   import { Injector } from '@angular/core';
   import { createCustomElement } from '@angular/elements';

   const element = createCustomElement(AppComponent, { injector });
   customElements.define('app-component', element);
   ```

3. **Kullanımı:**
   Artık bu bileşen herhangi bir HTML sayfasında kullanılabilir:
   ```html
   <app-component></app-component>
   ```

---

## **Angular CLI Custom Schematics**

Schematics, Angular CLI için özelleştirilmiş komutlar oluşturarak projelerde otomasyonu artırmayı sağlar. Örneğin, belirli bir yapı için bileşen veya servis şablonları oluşturabilirsiniz.

#### **Schematics Avantajları**
- **Otomasyon:** Tek bir komutla tekrarlayan işlemleri hızlandırır.
- **Standartlaştırma:** Ekip içinde kodun tutarlılığını sağlar.
- **Özelleştirme:** Projeye özel yapılandırmalar oluşturmanıza olanak tanır.

#### **Schematics ile Çalışmak**
1. **Yeni Bir Schematic Paketi Oluşturma:**
   ```bash
   npm install -g @angular-devkit/schematics-cli
   schematics blank --name=my-schematic
   cd my-schematic
   ```

2. **Schematic’i Özelleştirme:**
   Örneğin, bir bileşen oluşturma işlemini özelleştirmek için:
   ```typescript
   export function mySchematic(_options: any): Rule {
     return (tree: Tree) => {
       tree.create('/hello.txt', 'Hello, Schematics!');
       return tree;
     };
   }
   ```

3. **Test Etme ve Yayınlama:**
   ```bash
   npm run build
   schematics .:my-schematic
   ```

---

## **Angular Elements**

Angular Elements, Angular bileşenlerini framework bağımsız web bileşenlerine dönüştürmenizi sağlar. Bu, Angular uygulamalarının farklı ortamlarda (React, Vue veya Vanilla JS) kullanılabilmesini kolaylaştırır.

#### **Angular Elements ile Web Components Arasındaki Fark**
Angular Elements, Angular bileşenlerini kapsüller ve Web Components standartlarını kullanarak çalışır. Ancak Angular Elements, Angular bağımlılıklarını içerdiğinden genellikle daha ağırdır.

#### **Angular Elements Kullanımı**
1. **Setup:**
   Angular Elements modülünü ekleyin:
   ```bash
   npm install @angular/elements --save
   npm install @webcomponents/custom-elements --save
   ```

2. **Bileşen Tanımlama:**
   ```typescript
   import { Injector } from '@angular/core';
   import { createCustomElement } from '@angular/elements';

   @NgModule({
     declarations: [MyComponent],
     entryComponents: [MyComponent]
   })
   export class AppModule {
     constructor(private injector: Injector) {
       const element = createCustomElement(MyComponent, { injector });
       customElements.define('my-element', element);
     }

     ngDoBootstrap() {}
   }
   ```

3. **Kullanım:**
   Elde edilen element diğer projelerde bağımsız olarak kullanılabilir.

---

## **Stateful Component Design**

Stateful Component Design, bir bileşenin kendisine ait bir veri durumunu yönetmesi anlamına gelir. Bu yaklaşım, karmaşık kullanıcı arayüzleri ve bağımlı bileşenler için kritik öneme sahiptir.

#### **Stateful ve Stateless Bileşenler**
- **Stateful Bileşenler:** Veri durumunu kendi içinde tutar.
- **Stateless Bileşenler:** Durum bilgisi taşımaz ve sadece girdilere bağlı olarak çıktılar üretir.

#### **Stateful Bileşen Örneği**
1. **State Tanımlama:**
   ```typescript
   export class CounterComponent {
     counter: number = 0;

     increment() {
       this.counter++;
     }

     decrement() {
       this.counter--;
     }
   }
   ```

2. **Karmaşık Durum Yönetimi:**
   Karmaşık durumlar için RxJS kullanılabilir:
   ```typescript
   import { BehaviorSubject } from 'rxjs';

   export class TodoComponent {
     private todosSubject = new BehaviorSubject<string[]>([]);
     todos$ = this.todosSubject.asObservable();

     addTodo(todo: string) {
       const todos = this.todosSubject.getValue();
       this.todosSubject.next([...todos, todo]);
     }
   }
   ```

#### **Stateful ve Stateless Komponentler Arasında İletişim**
Stateful bir bileşen, stateless bileşenlere veri aktarabilir:
   ```html
   <app-stateless [data]="data"></app-stateless>
   ```
   
---
## **Complex Form Controls**

Angular’da karmaşık form kontrolleri, dinamik ve çok seviyeli yapılar oluşturmak için Reactive Forms ve Template-Driven Forms yapılarını kapsamlı bir şekilde kullanır. Özellikle iç içe geçmiş form grupları ve çok sayıda doğrulama gerektiren durumlar için önemlidir.

#### **Complex Form Kontrolleri İçin Reactive Forms**
1. **Reactive Forms Temelleri:**
   - Reactive Forms, Angular’ın `FormGroup`, `FormControl` ve `FormArray` sınıfları üzerine inşa edilmiştir.
   - Karmaşık yapılarda `FormGroup` ve `FormArray` bir arada kullanılabilir.

2. **Dinamik Form Alanları:**
   Bir form üzerinde kullanıcı girdilerine bağlı olarak yeni alanlar ekleme:
   ```typescript
   this.form = new FormGroup({
     name: new FormControl(''),
     addresses: new FormArray([]),
   });

   addAddress() {
     const addressGroup = new FormGroup({
       street: new FormControl(''),
       city: new FormControl(''),
     });
     (this.form.get('addresses') as FormArray).push(addressGroup);
   }
   ```

3. **Doğrulama:**
   Her bir form kontrolü için özel doğrulama kuralları eklenebilir:
   ```typescript
   const addressGroup = new FormGroup({
     street: new FormControl('', Validators.required),
     city: new FormControl('', Validators.maxLength(20)),
   });
   ```

4. **Template’de Kullanımı:**
   ```html
   <form [formGroup]="form">
     <input formControlName="name">
     <div formArrayName="addresses">
       <div *ngFor="let address of form.get('addresses').controls; let i = index" [formGroupName]="i">
         <input formControlName="street">
         <input formControlName="city">
       </div>
     </div>
   </form>
   ```

---

## **Angular Server-Side Rendering (SSR) ve Angular Universal**

Angular Server-Side Rendering (SSR), Angular uygulamasının ilk sayfa yükleme sırasında HTML’i sunucu tarafında render etmesini sağlar. Bu, performansı artırır ve arama motoru optimizasyonunu (SEO) geliştirir. Angular Universal, SSR’ı uygulamak için kullanılan Angular eklentisidir.

#### **SSR Avantajları**
- **SEO Uyumlu:** Arama motorları uygulamanın tüm içeriğini görebilir.
- **Hızlı İlk Yükleme:** Kullanıcıya anında render edilmiş HTML sunar.
- **Düşük Bant Genişliği Kullanımı:** JavaScript yüklenmeden önce içerik görüntülenebilir.

#### **Angular Universal ile SSR Kurulumu**
1. **Proje Kurulumu:**
   ```bash
   ng add @nguniversal/express-engine
   ```

2. **SSR için Express.js Sunucusu:**
   Angular Universal, Express.js tabanlı bir sunucu kullanır. `server.ts` dosyasını oluşturur:
   ```typescript
   import 'zone.js/node';
   import { ngExpressEngine } from '@nguniversal/express-engine';
   import * as express from 'express';
   import { AppServerModule } from './src/main.server';

   const app = express();
   app.engine('html', ngExpressEngine({
     bootstrap: AppServerModule,
   }));
   ```

3. **Build ve Çalıştırma:**
   ```bash
   npm run build:ssr
   npm run serve:ssr
   ```

---

## **Dynamic Components Component Factories**

Dinamik bileşenler, çalışma zamanında oluşturulan ve eklenen bileşenlerdir. Angular, `ComponentFactoryResolver` ve `ViewContainerRef` ile dinamik bileşen oluşturmayı destekler.

#### **Dinamik Bileşen Kullanımı**
1. **Dynamic Component Loader Service:**
   ```typescript
   @Injectable({ providedIn: 'root' })
   export class DynamicComponentLoaderService {
     constructor(private resolver: ComponentFactoryResolver) {}

     loadComponent(container: ViewContainerRef, component: any) {
       const factory = this.resolver.resolveComponentFactory(component);
       container.clear();
       return container.createComponent(factory);
     }
   }
   ```

2. **Bileşen Çağrımı:**
   ```typescript
   @Component({ template: '<ng-container #container></ng-container>' })
   export class AppComponent {
     @ViewChild('container', { read: ViewContainerRef }) container!: ViewContainerRef;

     constructor(private loader: DynamicComponentLoaderService) {}

     loadMyComponent() {
       this.loader.loadComponent(this.container, MyDynamicComponent);
     }
   }
   ```

3. **Template’de Kullanımı:**
   ```html
   <button (click)="loadMyComponent()">Load Component</button>
   <ng-container #container></ng-container>
   ```

---

## **Advanced Routing**

Angular Routing, karmaşık uygulama akışları için güçlü bir yönlendirme altyapısı sunar. Gelişmiş yönlendirme teknikleri, kullanıcı deneyimini iyileştirmek için dinamik yükleme, guard’lar ve yönlendirme verilerini içerir.

#### **Router Features**
1. **Lazy Loading:** Modüllerin yalnızca ihtiyaç duyulduğunda yüklenmesini sağlar.
   ```typescript
   const routes: Routes = [
     { path: 'feature', loadChildren: () => import('./feature/feature.module').then(m => m.FeatureModule) }
   ];
   ```

2. **Guards (CanActivate, CanDeactivate):** Yönlendirme öncesinde doğrulama ve izin kontrolü yapar.
   ```typescript
   canActivate(route: ActivatedRouteSnapshot): boolean {
     return this.authService.isLoggedIn();
   }
   ```

3. **Dinamik Parametreler:**
   ```typescript
   { path: 'details/:id', component: DetailsComponent }
   ```
   Parametre alma:
   ```typescript
   this.route.params.subscribe(params => {
     const id = params['id'];
   });
   ```

4. **Router Outlets ve Nested Routes:**
   İç içe bileşen yapıları için alt yönlendirme sağlar.
   ```html
   <router-outlet></router-outlet>
   ```

---


## **Global Error Handling**

Angular uygulamalarında global hata yönetimi, tüm uygulama boyunca meydana gelen hataları yakalamak ve bunları yönetmek için kullanılır. Bu, kullanıcı deneyimini geliştirmek ve hataları merkezi bir şekilde işlemek için önemlidir.

#### **Global Error Handling İçin Temel Yaklaşım**
1. **ErrorHandler Servisini Kullanmak:**
   Angular’da yerleşik `ErrorHandler` sınıfı özelleştirilebilir.
   ```typescript
   @Injectable()
   export class GlobalErrorHandler implements ErrorHandler {
     handleError(error: any): void {
       // Hataları loglamak için
       console.error('Global Error:', error);
       // Özel hata işlemleri yapılabilir
     }
   }
   ```

2. **AppModule’de Tanımlama:**
   ```typescript
   @NgModule({
     providers: [
       { provide: ErrorHandler, useClass: GlobalErrorHandler }
     ]
   })
   export class AppModule {}
   ```

3. **HttpInterceptor ile Hata Yönetimi:**
   HTTP isteklerinde meydana gelen hataları yakalamak için:
   ```typescript
   @Injectable()
   export class HttpErrorInterceptor implements HttpInterceptor {
     intercept(req: HttpRequest<any>, next: HttpHandler): Observable<HttpEvent<any>> {
       return next.handle(req).pipe(
         catchError((error: HttpErrorResponse) => {
           console.error('HTTP Error:', error);
           return throwError(error);
         })
       );
     }
   }
   ```

---

## **Global State Management**

Angular’da global state management, uygulama genelinde paylaşılan durumların (state) yönetimini sağlar. Redux, NgRx, Akita ve RxJS gibi araçlarla karmaşık durumların işlenmesi mümkündür.

#### **NgRx Kullanımı**
1. **Store Yapısı:**
   - Global bir store, uygulamanın durumunu merkezi bir yerde tutar.
   - Aksiyonlar, durumun nasıl değişeceğini belirtir.

2. **Store Kurulumu:**
   ```bash
   ng add @ngrx/store
   ```
   Store tanımlama:
   ```typescript
   export interface AppState {
     counter: number;
   }

   export const initialState: AppState = {
     counter: 0,
   };

   const _counterReducer = createReducer(
     initialState,
     on(increment, state => ({ ...state, counter: state.counter + 1 })),
     on(decrement, state => ({ ...state, counter: state.counter - 1 }))
   );

   export function counterReducer(state: any, action: Action) {
     return _counterReducer(state, action);
   }
   ```

3. **Store Kullanımı:**
   ```typescript
   constructor(private store: Store<{ counter: number }>) {}

   increment() {
     this.store.dispatch(increment());
   }

   decrement() {
     this.store.dispatch(decrement());
   }

   getCounter() {
     this.store.select('counter').subscribe(data => console.log(data));
   }
   ```

---

## **CSS Preprocessing**

Angular uygulamalarında CSS preprocessing, Sass veya LESS gibi araçlarla daha güçlü ve esnek stiller yazmayı sağlar. Bu yaklaşım, bileşen düzeyinde düzenli ve yeniden kullanılabilir stiller oluşturmak için kullanılır.

#### **Sass Kullanımı**
1. **Angular Projesinde Sass Aktifleştirme:**
   ```bash
   ng config schematics.@schematics/angular:component.styleext scss
   ```
   veya projenin oluşturulması sırasında:
   ```bash
   ng new my-app --style=scss
   ```

2. **Değişkenler ve Mixins:**
   ```scss
   $primary-color: #3498db;

   @mixin flex-center {
     display: flex;
     justify-content: center;
     align-items: center;
   }

   .button {
     background-color: $primary-color;
     @include flex-center;
   }
   ```

3. **Component-Based Stiller:**
   Angular bileşenlerinde `styleUrls` yerine `styles` kullanarak Sass ile yazılmış stilleri ekleyebilirsiniz:
   ```typescript
   @Component({
     selector: 'app-root',
     templateUrl: './app.component.html',
     styleUrls: ['./app.component.scss']
   })
   export class AppComponent {}
   ```

---

## **Modular Architecture Micro Frontends**

Modüler mimari ve mikro ön yüz yapıları, Angular uygulamalarını daha ölçeklenebilir ve bağımsız hale getirmek için kullanılır.

#### **Modüler Mimari:**
1. **Feature Modülleri:**
   Angular projelerinde her özelliği ayrı bir modüle ayırmak, bağımsız geliştirme ve bakım kolaylığı sağlar.
   ```typescript
   @NgModule({
     declarations: [FeatureComponent],
     imports: [CommonModule],
     exports: [FeatureComponent]
   })
   export class FeatureModule {}
   ```

2. **Shared ve Core Modülleri:**
   - Shared Module: Yeniden kullanılabilir bileşenler, direktifler, pipe’lar içerir.
   - Core Module: Tek bir kez yüklenmesi gereken servisler ve global bileşenler barındırır.

#### **Micro Frontends:**
1. **Module Federation ile Mikro Ön Yüzler:**
   Angular CLI’da Webpack Module Federation’ı etkinleştirerek bağımsız olarak geliştirilen modülleri bir araya getirebilirsiniz:
   ```bash
   ng add @angular-architects/module-federation
   ```

2. **Host ve Remote Yapıları:**
   - Host uygulama, diğer mikro ön yüzleri yükler.
   - Remote uygulamalar, belirli bir özelliği veya modülü sağlar.
   ```typescript
   // Remote
   @NgModule({
     declarations: [RemoteComponent],
     exports: [RemoteComponent]
   })
   export class RemoteModule {}
   ```

3. **Dynamic Import:**
   Mikro ön yüzleri dinamik olarak yüklemek için `loadRemoteModule` kullanılır:
   ```typescript
   loadRemoteModule({
     type: 'module',
     remoteEntry: 'http://localhost:3000/remoteEntry.js',
     exposedModule: './Module'
   }).then(m => m.RemoteModule);
   ```

---

## **Custom Decorators**  
Custom decorators, Angular'da, sınıf, metot veya özelliklere işlevsellik eklemek için kullanılan özelleştirilmiş dekoratörlerdir. TypeScript, decorator’ları yazmanıza olanak sağlar. Örneğin, bir metodun çağrılma sayısını izlemek için basit bir decorator yazalım:

```typescript
function LogMethodCalls(target: any, propertyName: string, descriptor: PropertyDescriptor) {
  const originalMethod = descriptor.value;
  descriptor.value = function(...args: any[]) {
    console.log(`Method ${propertyName} was called with args: ${JSON.stringify(args)}`);
    return originalMethod.apply(this, args);
  };
  return descriptor;
}

class ExampleService {
  @LogMethodCalls
  someMethod(name: string) {
    console.log(`Hello, ${name}`);
  }
}
```

Burada, `LogMethodCalls` dekoratörü, `someMethod` fonksiyonunu çağırmadan önce, çağrının argümanlarını logluyor. Bu sayede her metod çağrısını izleyebilirsiniz.

---

## **WebSockets**  
WebSockets, istemci ve sunucu arasında sürekli bir bağlantı kurar, böylece anlık veri aktarımı sağlanabilir. Bu özellik, özellikle chat uygulamaları, canlı skorlar, anlık bildirimler gibi uygulamalar için çok kullanışlıdır. Örneğin, Angular’da WebSocket kullanarak bir chat uygulaması için basit bir bağlantı kurabiliriz:

1. **WebSocketService**:
```typescript
import { Injectable } from '@angular/core';
import { WebSocketSubject } from 'rxjs/webSocket';

@Injectable({
  providedIn: 'root',
})
export class WebSocketService {
  private socket$: WebSocketSubject<any>;

  constructor() {
    this.socket$ = new WebSocketSubject('ws://example.com/chat');
  }

  sendMessage(message: string) {
    this.socket$.next({ message });
  }

  getMessages() {
    return this.socket$.asObservable();
  }
}
```

2. **Component**:
```typescript
import { Component, OnInit } from '@angular/core';
import { WebSocketService } from './web-socket.service';

@Component({
  selector: 'app-chat',
  templateUrl: './chat.component.html',
})
export class ChatComponent implements OnInit {
  messages: string[] = [];

  constructor(private webSocketService: WebSocketService) {}

  ngOnInit() {
    this.webSocketService.getMessages().subscribe((msg) => {
      this.messages.push(msg);
    });
  }

  sendMessage(msg: string) {
    this.webSocketService.sendMessage(msg);
  }
}
```

Bu örnekte, Angular bileşeni, WebSocketService ile gerçek zamanlı olarak mesajları alır ve gönderir.

---

## **Code Splitting**  
Code Splitting, uygulamanın tüm JavaScript kodunu başta yüklemek yerine, ihtiyaca göre yüklenmesini sağlar. Bu, sayfa yükleme süresini kısaltır. Angular, Lazy Loading ile bunu destekler. Örneğin, bir modül sadece ihtiyaç duyulduğunda yüklenebilir.

```typescript
// app-routing.module.ts
const routes: Routes = [
  {
    path: 'feature',
    loadChildren: () => import('./feature/feature.module').then(m => m.FeatureModule)
  },
];
```

Bu örnekte, `FeatureModule` sadece kullanıcı `feature` yoluna gittiğinde yüklenir.

---

## **Web Components**  
Web Components, bağımsız, yeniden kullanılabilir bileşenler oluşturmanıza olanak tanır. Angular bileşenleri, Web Component olarak dışarıya sunulabilir. Örneğin, bir Angular bileşenini Web Component’e dönüştürme:

```typescript
import { Injector, DoBootstrap } from '@angular/core';
import { createCustomElement } from '@angular/elements';
import { AppComponent } from './app.component';

@NgModule({
  declarations: [AppComponent],
  imports: [BrowserModule],
  bootstrap: [],
})
export class AppModule implements DoBootstrap {
  constructor(private injector: Injector) {}

  ngDoBootstrap() {
    const el = createCustomElement(AppComponent, { injector: this.injector });
    customElements.define('app-element', el);
  }
}
```

Burada, `AppComponent` bir Web Component olarak tanımlanır ve `app-element` olarak kullanılabilir.

---

## **Angular CLI Custom Schematics**  
Angular CLI Custom Schematics, yeni proje şablonları, component şablonları veya genel proje yapısını değiştiren özel komutlar oluşturmanıza olanak tanır. Örneğin, bir yeni component oluşturduğunuzda bazı dosyaların da otomatik olarak eklenmesini isteyebilirsiniz.

```typescript
import { Rule, SchematicContext, Tree } from '@angular-devkit/schematics';

export function myCustomComponent(options: any): Rule {
  return (tree: Tree, _context: SchematicContext) => {
    tree.create('/src/app/' + options.name + '.component.ts', 'Component content here');
    return tree;
  };
}
```

Burada, özel bir schematic ile yeni bir component dosyası oluşturulmuştur.

---

## **Angular Elements**  
Angular Elements, Angular bileşenlerini Web Components formatında dışa aktarır. Bu sayede Angular bileşenlerini başka framework’ler veya saf HTML sayfalarında da kullanabilirsiniz. Örneğin:

```typescript
import { Injector, DoBootstrap } from '@angular/core';
import { createCustomElement } from '@angular/elements';
import { MyComponent } from './my.component';

@NgModule({
  declarations: [MyComponent],
  imports: [BrowserModule],
  bootstrap: [],
})
export class AppModule implements DoBootstrap {
  constructor(private injector: Injector) {}

  ngDoBootstrap() {
    const customElement = createCustomElement(MyComponent, { injector: this.injector });
    customElements.define('my-angular-element', customElement);
  }
}
```

Bu örnekte, `MyComponent` artık `my-angular-element` olarak bağımsız bir web bileşeni olarak kullanılabilir.

---

## **Stateful Component Design**  
Stateful component design, bileşenlerin durumunu kendi içinde yönetmesine olanak tanır. Bu tür bileşenler, yalnızca içsel durumlarını kontrol eder ve dışarıdan gelen verilerle etkileşimde bulunurlar. Örnek olarak:

```typescript
@Component({
  selector: 'app-toggle',
  template: `<button (click)="toggle()">Toggle State</button><p>{{ state }}</p>`
})
export class ToggleComponent {
  state = 'OFF';

  toggle() {
    this.state = this.state === 'OFF' ? 'ON' : 'OFF';
  }
}
```

Burada, `ToggleComponent` bileşeni kendi durumunu (`state`) yönetiyor ve butona tıklayarak durumu değiştiriyor.

---
