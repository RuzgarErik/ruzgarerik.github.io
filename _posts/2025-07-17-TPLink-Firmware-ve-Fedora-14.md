---
layout: post
---


TP-Link TD-9980V3 Firmware build etmek için README dosyasında Fedora 14 ile başarılı olarak derlendiği bildirilmiştir. Bunun için Oracle
VirtualBox kullanarak Feoora 14 yükledim.


Fedora 14 sisteminin 2010 yılından kalması bu sistemle 2025 yılında çalışmamızı zorlaştırıyor bunun için birkaç düzenleme yaptım.


{% highlight ruby %}

cd /etc/yum.repos.d/

sudo mv fedora.repo fedora.repo.bak #repo dosyaları yedeklenir
sudo mv fedora-updates.repo fedora-updates.repo.bak


{% endhighlight %}



nano fedora-archive.repo

```bash
[fedora]
name=Fedora 14 - x86_64
failovermethod=priority
baseurl=http://archives.fedoraproject.org/pub/archive/fedora/linux/releases/14/Fedora/x86_64/os/
enabled=1
gpgcheck=0

[updates]
name=Fedora 14 - x86_64 - Updates
failovermethod=priority
baseurl=http://archives.fedoraproject.org/pub/archive/fedora/linux/updates/14/x86_64/
enabled=1
gpgcheck=0
```



```
```
