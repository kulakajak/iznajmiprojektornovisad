# iznajmiprojektornovisad

Download

~~~
git clone git@github.com:kulakajak/iznajmiprojektornovisad.git
~~~

Project is on gh-pages. Deploy simply by git push

~~~
git push
~~~

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
find assets/references/* -maxdepth 0 -type f -printf "%TY-%Tm-%TdT%TT %p\n" | sort -nr  | cut -d' ' -f2- | awk '{print "\""$0"\","}'
```
