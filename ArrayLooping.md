## Pengulangan While 

## Dasar 

```cpp
#include<iostream>
using namespace std;
int main(){
    int jumlahMahasiswa = 0 ;
    
    while (jumlahMahasiswa<10){
        cout << jumlahMahasiswa<<" Mahasiswa yang saat ini ada di kampus\n";
        jumlahMahasiswa++;
    }
    return 0;
}
```

```cpp
#include <iostream>
using namespace std;

int main() {
  int langkah = 0;
  int diTujuan = 0;
  
  while (diTujuan == 0) {
    cout <<"Kamu telah melangkah " << langkah << "Langkah \n";
    
    if(langkah == 50) {
        diTujuan = 2;
    }
    
    langkah++;
  }
  return 0;
}
```
## Deret ;

```cpp
#include<iostream>
using namespace std;

int main (){
    int kali = 0;
    
    while (kali<10){
        cout << kali * 2 << " Merupakan bilangan yang  di kali : " << kali << "x2\n";
        kali++;
    }
    return 0;
}
```


