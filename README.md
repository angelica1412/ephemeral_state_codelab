# ephemeral_state_codelab

**Perbedaan antara App State dan Ephemeral State**
Sebenarnya pada saat pertama kali saya melihat tampilan UI antara app state dan ephemeral state terlihat cukuplah mirip di mana sama-sama menampilkan nilai counter value yang dapat berubah ketika tombol increment atau decrement (pada App state) ditekan. Namun perbedaannya adalah pada code dan fungsi dari masing-masing state. 

Pada App state ini menggunakan scope model sebagai library yang digunakan dalam pengembangan aplikasi Flutter untuk mengelola dan berbagi keadaan (state) aplikasi secara terpusat. State ini bersifat keseluruhan di mana state ini dapat mengakses seluruh bagian atau fitur yang ada pada aplikasi tersebut. Pada state ini, data counter dikelola secara terpusat dalam class CounterModel, memungkinkan penggunaan dan akses yang terpusat ke seluruh aplikasi. Perubahan state ini secara otomatis memicu pembaruan pada semua widget yang bergantung pada data tersebut.

Ephemeral State, nilai counter disimpan dalam widget-stateful CounterWidget, sehingga status ini hanya berlaku dalam konteks widget tersebut. Meskipun UI-nya dapat memperbarui nilai counter ketika tombol Increment ditekan, perubahan ini hanya memengaruhi widget ini dan tidak dapat dibagikan atau diakses dari luar widget tersebut. 

Kesimpulan: 
App State memungkinkan pengelolaan data yang lebih terpusat dan pembagian yang efisien, yang berguna untuk keadaan aplikasi yang bersifat global. Sementara Ephemeral State cocok untuk keadaan yang bersifat sementara dan terbatas pada widget tertentu. Pemilihan antara keduanya tergantung pada kompleksitas dan skala aplikasi yang sedang dikembangkan.


**Kelebihan Menggunakan App State Management**
1. Pengelolaan State yang Kompleks:
   Aplikasi yang lebih besar seringkali melibatkan pengelolaan state yang kompleks, seperti otentikasi pengguna, pengelolaan isi keranjang belanja, atau pengaturan aplikasi global. Manajemen State Aplikasi membantu Anda mengelola state-state kompleks ini secara efisien, sehingga Anda dapat mengintegrasikan logika bisnis yang rumit tanpa membuat tampilan menjadi rumit.
2. Skalabilitas:
    Saat aplikasi akan dikembangkan, kebutuhan pengelolaan data dan state menjadi lebih kompleks. Manajemen State Aplikasi dirancang untuk mengatasi perubahan ini secara efisien. Ini memastikan bahwa aplikasi tersebut dapat dengan mudah menambahkan fitur baru, memenuhi perubahan aturan bisnis yang berkembang, dan memelihara aplikasi tanpa memperkenalkan beban teknis yang tidak perlu.
3. Pembaruan Otomatis
   Ketika terdapat state aplikasi berubah, seperti status otentikasi pengguna atau isi keranjang belanja, maka perubahan ini secara otomatis diteruskan ke semua bagian aplikasi. Hal ini menghasilkan pengalaman pengguna yang responsif dan konsisten tanpa perlu melakukan sinkronisasi data manual. Dengan demikian, data seperti status otentikasi pengguna atau isi keranjang belanja, dikelola secara terpusat di luar widget tempat digunakan. Ketika data berubah, perubahan tersebut secara otomatis diteruskan ke seluruh komponen aplikasi yang bergantung pada data tersebut, sehingga pengguna tidak perlu merasakan penundaan atau data yang tidak sesuai. 
