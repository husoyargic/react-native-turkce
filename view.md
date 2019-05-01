# View

Belki de en temel component. Android'deki `android.view`, IOS'daki `UIView`. HTLM'deki karşılığı `div` diyebiliriz. Ekranımızı temel anlamda şekillendiren UI elementi.

[Resmi dökümanda](https://facebook.github.io/react-native/docs/view.html) tüm propslarını görebilirsiniz. Zaten yapacağımız örneklerde bir çok kez kullanacağız. Burada gözden kaçabilecek bir özelliğinden bahsetmek istiyorum.

View componenti mount edilir edilmez, **onLayout** eventi tetiklenir.

```javascript
<View  onLayout={this._handleLayout} />
```

Burada fonksiyonumuzun bir tane obje tipinde parametresi olur.

```javascript
_handleLayout=(e)=>{
   const { x, y, width, height } = e.nativeEvent.layout
}
```

Burada Vİew componentimizin, parent elemente göre x ve y konumunu, genişlik ve uzunluk bilgilerine erişebilirsiniz. Animasyon kısmında göreceğimiz, LayoutAnimation yöntemini kullanırken bayağı işe yarıyor.

