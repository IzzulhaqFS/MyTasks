# MyTasks
## Screenshot Aplikasi
![myTask](https://user-images.githubusercontent.com/57482751/222904738-59507268-204c-41c3-9395-e5d21983d084.png)

## Cara Kerja Aplikasi
Aplikasi MyTasks akan mengambil input berupa string yang dimasukkan melalui sebuah entry kemudian menekan tombol **Add**. Setelah menekan tombol **Add** string tersebut akan dimasukkan ke dalam collection dan ditampilkan dalam bentuk list menggunakan **CollectionView**.

### MainPage.xaml
File xaml ini berfungsi untuk mendefinisikan UI dari aplikasi ini. Terdapat beberapa view yang digunakan di aplikasi ini, diantaranya
1. Image
2. Label
3. Entry
4. Button
5. CollectionView

### MainPage.xaml.cs
Kelas yang berfungsi untuk mengontrol UI dari file **MainPage.xaml**. Kelas ini akan menginisialisasikan komponen view dari **MainPage.xaml** dan mendefinisikan **BindingContext** untuk menghubungkan UI dengan View Model di kelas **MainViewModel.cs**.

### MainViewModel.cs
Kelas View Model yang digunakan untuk mengatur tampilan aplikasi dan mengontrol event yang terjadi ketika ada interaksi dengan view. Kelas ini mengimplementasikan **ObservableObject** dan memiliki dua **ObservableProperty** yakni sebuah **ObservableCollection** bernama items yang berisi data-data string dan sebuah string bernama item yang digunakan untuk menyimpan input dari entry. Kemudian, kelas ini juga memiliki dua **RelayCommand** yakni sebuah fungsi **Add** dan **Delete**. Fungsi **Add** dipanggil ketika tombol **Add** ditekan, dan akan memasukkan input yang ada di entry ke dalam collection untuk ditampilkan melalui **CollectionView**. Fungsi **Delete** akan dipanggil ketika salah satu item di **CollectionView** di-*swipe* ke kiri dan muncul tombol **Delete** sehingga item yang dipilih akan dihapus dari collection.
