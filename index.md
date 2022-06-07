
## Logistic Regression 

Yazar: Mustafa Eroğlu

Tarih: 7 Haziran 2022

<p>
Bu projede, belirli bir internet kullancısının bir şirketin web sitesindeki bir reklamı tıklayıp tıklamadığını gösteren sahte bir reklam veri seti ile çalıştım. Kullanıcının özelliklerinden yola çıkarak bir reklama tıklayıp tıklamadığını tahmin edecek bir model oluşturmaya çalıştım.
</p>

<p> Verileri keşfedelim.</p>

```
df.head()
```

![image](/img/df-logistic.png)


<p>Age histogram grafiği oluşturalım.</p>

```
sns.set_style('whitegrid')
df['Age'].hist(bins=30)
plt.xlabel('Age')
```
![image](/img/age-HİST.png)

<p>Age vs Area Income jointplot grafiği oluşturalım.</p>

```
sns.jointplot(x='Age',y='Area Income',data=df)
```
![image](/img/age-AREA-INCOME.png)

<p>Age vs Daily Time Spent on Site jointplot grafiği oluşturalım ve kde dağılımlarını gözlemleyelim. </p>

```
sns.jointplot(x='Age',y='Daily Time Spent on Site',data=df,color='red',kind='kde')
```
![image](/img/daily-time-age.png)

<p> Daily Time Spent on Site vs Daily Internet Usage jointplot grafiği oluşturalım. </p>

```
sns.jointplot(x='Daily Time Spent on Site',y='Daily Internet Usage',data=df,color='green')
```
![image](/img/daily-time-net-usage.png)

<p> Modeli train ve test olarak bölüp eğitiyoruz. Classification report:  </p>

![image](/img/logistic-report.png)


<p>Okuduğunuz için teşekkürler </p>


