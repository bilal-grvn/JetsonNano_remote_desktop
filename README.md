# JetsonNano_remote_desktop

<h4 align="left">
Yazar : Bilal GÜREVİN👋👋
</h4>

## `Jetson Nano`'ya farklı bir PC de uzak masaüstü bağlantısını VNC server üzerinden gerçekleştirebileceğiniz temel işlemleri aşağıda bulabilirsiniz.

***************************************************************
***************************************************************


# 🚀 VINO KURULUMU

Aşağıdaki satırı jetson nano terminal ekranında yazıyoruz.

```sh
sudo apt-get install vino
```

kurulumdan sonra yeni bir terminal akranında aşağıdaki satırları yazarak vino yu aktif ederiz ve diğer PC'den bağlantı için beklemeye başlar.

```sh
/usr/lib/vino/vino-server
```

Ama öncesinde aşağıdaki resimde gösterildiği gibi Jetson Nano tarafında ayarlar kısmından paylaşım izinlerini vermemiz gerekmektedir.

<p align="center">
  <img width="600" height="400" src="img/sharing_settings.png?raw=true">
</p>

izinleri de verdikten sonra diğer PC tarafında VNC açılır. Buraya IP adresini girer ve enter tuşuna basarız.

Bundan sonra Jetson Nano da bağlantıya izin vermek için bir ekran çıkacaktır. Kabul etmemiz sonucunda bağlantı geçekleşecektir.

`ifconfig` yazarak Jetson Nano nun IP adresini öğrenebiliriz.

Örneğin bende `inet 192.168.1.113` şeklinde çıktı.

<p align="center">
  <img width="500" height="300" src="img/vnc_IP.png?raw=true">
</p>





# 🚀 NOT
PC tarafında bazen `encrypted` ile ilgili bir hata verebilir.

Bu yüzden Jetson Nano terminalinde aşağıdaki satırı yazmamız sorunu çözebilir.

```sh
gsettings set org.gnome.Vino require-encryption false
```

Ayrıca Jetson Nano tarafında ekran çözünürlüğünü azaltmamız diğer PC'den erişim hızını arttıracaktır.