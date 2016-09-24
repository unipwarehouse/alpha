---
title: Daah CMS, Hello Jekyll!
date: 2016-06-19
categories: misc
---
Selama beberapa tahun mengenal dunia web development dan pembangunan website, saya hanya mencoba menggunakan *Content Maganement System* atau CMS untuk membangun website. Tapi sekarang saya beralih ke Jekyll.

### Daah CMS

Sebenarnya, ada beberapa metode lain *sih* selain menggunakan CMS, seperti menggunakan framework web app seperti Ruby on Rails atau yang berbasis Javascript seperti node dipadukan dengan React atau Angular, tapi karena saya orangnya sangat visual dan pusing *banget* melihat kode yang sulit terbaca oleh manusia, lagi-lagi saya harus kembali menggunakan CMS.

CMS sering digunakan perusahaan atau personal yang ingin membangun website dan mengelola isinya secara mandiri. Kalau teman-teman tahu Wordpress, Drupal, Joomla, yup itu salah satu beberapa CMS yang sering digunakan sekarang ini. Biasanya untuk mengedit konten website, pengembang CMS menyertakan antarmuka Dashboard bagi administrator dan moderator website. Mengaksesnya pun kalau sudah dalam skala produksi ya harus *online* dulu, alias menggunakan jaringan internet. Tapi saya pribadi makin ke sini makin merasa ribet dengan proses seperti itu, karena jujur saya masih menggunakan jaringan mobile broadband yang bisa dikatakan belum se-stabil jaringan nirkabel. Serta proses membuka Dashboard yang tergantung dengan kecepatan internet, bisa hanya beberapa detik, bisa sampai bermenit-menit hanya untuk proses satu kali klik. *Hedeuh*.

Kalau saya dulu, untuk mengakali kendala jaringan internet, saya harus menyiapkan environment development secara lokal atau offline. Jadi nantinya untuk melihat hasil tampilan websitenya biasanya cukup dengan mengakses *localhost* di browser saya. Tapi, lagi-lagi saya harus ribet dengan keperluan server lokal seperti Apache, PHP, MySQL serta menyesuaikan *file permission* yang sangat bervariasi dari tiap CMS. Pokoknya bisa capek duluan hanya untuk urusan teknisnya.

Sampai suatu hari saya mengenal nama [Jekyll](http://jekyllrb.com) dengan kesederhanaannya dalam proses membangun website.

### Hello Jekyll

Jekyll dikembangkan oleh penyedia hosting berbasis git, [Github](http://github.com), yang ditulis dengan bahasa pemrograman Ruby. Jekyll ini bisa dikatakan CMS, tapi bedanya Jekyll membangun struktur website dengan men-*generate* tiap halaman yang ada di website secara individual dengan format file `html` atau sering disebut dengan halaman statis. Jekyll sebenarnya diprioritaskan untuk mereka yang ingin membangun website blog yang kontennya sebagian besar berupa artikel. Namun karena fleksibilitas yang ditawarkan Jekyll kepada para web developer, akhirnya banyak website yang dibangun dengan Jekyll yang berfungsi lebih dari sekedar blog dengan bermacam jenis konten dan fitur.

Lalu bagaimana dengan masalah pribadi saya soal jaringan internet tadi? Tenang. Jekyll mengharuskan kita menginstall tool untuk keperluan development/ pengembangan website. Dengan tool ini Jekyll akan mengolah file yang ada di folder tertentu untuk dirender menjadi struktur website kita, walaupun hanya satu file `index.html` saja! Artinya, di manapun lokasi drive kita membuat projek website, entah di `C:`, di `D:` bagi pengguna Windows, atau di `Home`, di subfolder dll, kita tetap bisa membangunnya hanya dengan mengetik *command line* `jekyll new nama_projek` dan `enter`. Kalau saya pribadi, biasanya saya mulai dengan membuat template `html`nya yang sebelumnya sudah saya desain dulu. Lalu jika saya rasa desain sudah ok, tanpa perlu basa-basi saya ketik `jekyll serve` pada terminal atau command prompt jika di Windows, dan `enter`. Jekyll akan men-*generate* file-file yang ada di satu folder projek tadi menjadi struktur website berdasarkan `URL`nya dan disediakan di `127.0.0.1:4000` atau biasa kita ketik dengan `localhost:4000`. Seketika hasil kerja kita dalam membangun website dapat kita lihat secara lokal dan **offline** tanpa ribet memikirkan masalah PHP MySQL, dst.

Bahkan jika perlu, kita bisa sewaktu-waktu memindahkan folder projek tadi di lokasi mana saja dan menjalankannya dimanapun komputer yang terinstall tool Jekyll, tidak seperti CMS yang harus berada di lokasi tertentu.

Saya juga menggunakan program version control [Git](http://git-scm.com), untuk mengelola perubahan dan versioning website saya agar lebih mudah. Yang lebih penting lagi, jika terjadi kesalahan selama proses development website, saya bisa mengembalikannya ke keadaan sebelum terjadi kesalahan. Ini sama seperti fungsi *undo* dan *redo* dalam setiap program pengolah data, hanya saja lebih kompleks.

### Tools

Tools yang diperlukan mulai dari pengembangan website sampai dengan publishing atau produksi hanya terminal atau command prompt dan program teks editor saja, seperti Notepad, Notepad++, Textmate, Atom, Bracket, dan saya pribadi menggunakan Sublime Text.

Dalam publishing, teman-teman tidak usah pusing dengan format penulisan karena Jekyll mendukung konten dengan format `markdown` dan `textile` (dengan plugin) yang sangat mudah untuk dipelajari.

### Hosting

Untuk hosting, Pengembang Jekyll sendiri menyediakan layanan gratis [Github Pages](http://pages.github.com), yaitu layanan hosting gratis dengan tool Jekyll yang sudah terinstall di dalamnya dan saya pribadi menggunakan ini. Jadi saya hanya perlu mengupload dependesi Jekyll dan selanjutnya Github Pages yang akan men-*generate* websitenya. Namun karena Github sendiri mengharuskan penggunanya menggunakan program Git, maka kita harus belajar pemakaian dasarnya jika ingin menggunakan layanan Github Pages.

Tapi kalau teman-teman ingin menggunakan hosting seperti pada umumnya juga bisa, seperti di GoDaddy, Amazon, Sidepoint, Media Temple, Google Firebase dengan gratis SSL + hosting 1 GB atau penyedia hosting dalam negeri seperti Niagahoster, Dewaweb, Masterweb, dll. Dengan hanya mengupload semua file yang terletak di folder `_site` ke tempat hosting kita, kita sudah bisa membuat sebuah website berjalan tanpa perlu khawatir soal kemampuan server. Karena semua file yang kita upload bersifat statis, sudah pasti semua web server akan dengan mudah menampilkannya di setiap browser pengguna.

### Langkah Selanjutnya

Selanjutnya, teman-teman bisa langsung mencoba menggunakan Jekyll dengan beberapa perintah saja. Ingat, komputer harus [memenuhi kebutuhan](https://jekyllrb.com/docs/installation/#requirements) agar proses berjalan dengan lancar.

{% highlight shell %}
~ $ gem install jekyll bundler
~ $ jekyll new nama_projek
~ $ cd nama_projek
~/nama_projek $ bundle install
~/nama_projek $ bundle exec jekyll serve
# => Lalu buka http://localhost:4000
{% endhighlight %}

Atau kunjungi [dokumentasi Jekyll](http://jekyllrb.com/docs/home/) untuk belajar lebih banyak bagaimana penggunaannya agar website terasa lebih dinamis.

Banyak yang masih bisa dilakukan dengan Jekyll terlebih lagi karena Jekyll sendiri adalah program opensource yang artinya dapat dikembangkan oleh semua orang tanpa khawatir soal lisensi. Ada beberapa hal yang mungkin bisa dilakukan untuk lebih membuat website Jekyll terlihat lebih dinamis, seperti:

- Menambah `contenttype` (istilah jenis konten selain artikel)
- Memasang plugin Disqus untuk form komentar dan menambah comment counter
- Menambah fungsi unlimited scroll dengan AJAX
- Menginstall plugin Jekyll Admin untuk merasakan tampilan Dashboard seperti CMS pada umumnya
- Export konten dari CMS lama seperti Wordpress, ke Jekyll
- Menggunakan custom domain untuk website Github Pages kita

### Kesimpulan

Ini hanya tulisan saya sebagai pengguna Jekyll sekaligus testimonial. Intinya saya cukup puas dengan tool Jekyll untuk kebutuhan publishing dan pengembangan website saya. Yang saya inginkan adalah CMS yang fleksibel, minim syarat, dan cukup mudah digunakan. Soal kekurangan pasti ada, tapi seiring dengan waktu para pengembang Jekyll menambahkan fitur-fitur baru yang sangat membantu dalam mengembangkan website menjadi kaya akan konten yang bervariasi. Yang penting saya bisa fokus dengan konten saya tanpa khawatir dengan bermacam-macam keperluan server website convensional.