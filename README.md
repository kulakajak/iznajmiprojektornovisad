# iznajmiprojektornovisad

Download

~~~
git clone git@github.com:kulakajak/iznajmiprojektornovisad.git
~~~

Project is on gh-pages. Deploy simply by git push

~~~
git push
~~~

When using non default ssh key you can use `kgithub`
```
# .ssh/config
Host kgithub.com
  Hostname github.com
  IdentityFile ~/.ssh/id_rsa_kulakajak

git clone git@kgithub.com:kulakajak/iznajmiprojektornovisad.git
cd iznajmiprojektornovisad
git pull

# push does not work since it uses default key, not for kgithub, so we need to:
ssh-add ~/.ssh/id_rsa_kulakajak
```

To add reference image you can follow this steps

```
cp ~/Downloads/image.jpg assets/references/any_name.jpg

# resize
image.rb resize_if_gt 680 assets/references/*.jpg

# add watermark
image.rb watermark iznamljivanjeprojektoranovisad.in.rs assets/references/*.jpg

# change date
touch -d "1 month ago" "assets/references/uporedni prikaz belog i crnog projektora iza.jpg",

# to copy to javascript
gfind assets/references/* -maxdepth 0 -type f -printf "%TY-%Tm-%TdT%TT %p\n" | sort -nr  | cut -d' ' -f2- | awk '{print "\""$0"\","}'
```
