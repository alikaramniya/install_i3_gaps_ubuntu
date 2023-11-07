# install_i3_gaps_ubuntu

### اول از همه من برای نصب کردن i3_gaps در اوبونتو از لینک پایین کمک گرفتم

[link](https://devicetests.com/install-i3-gaps-ubuntu-22-04-jammy-jellyfish)

###توی قدم اول ما دستور پایین رو توی اوبونتو ۲۲ خود وراد میکنیم که اینا برای ما نصب بشن 


```

sudo apt install meson asciidoc
```

### بعد از اتمام ما دستور پایین رو اجرا میکنیم که یک سری نیازمندی ها برای اون نصب بشن

``` sudo apt install libxcb-render0-dev libxcb-shape0-dev libxcb-xfixes0-dev ```

### که من اینو از این ادرس اوردم 
[link](https://github.com/nannou-org/nannou/issues/746)

### بعد از نصب کردن این نیاز مندی ها با دستورای پایین رو اجرا کنید

```
mkdir /tmp/build
cd /tmp/build
```

### بعد از نصب کردن این موارد هم الان مخزن زیر رو clone کنید
```
git clone https://www.github.com/Airblader/i3 i3-gaps
```
### بعد از اتمام این مرحله دستورای زیر رو اجرا کنید و تمام :)

```
cd i3-gaps
git checkout gaps && git pull
meson -Ddocs=true -Dmans=true ../build
meson compile -C ../build
sudo meson install -C ../build
```
