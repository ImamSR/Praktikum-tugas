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
## Penggunaan break 

```cpp
#include <iostream>
using namespace std;

struct warga_kos{ 
	int id;
    string nama;
    string kamar;
    string pekerjaan;
    
};
int main()
{
	 warga_kos warga[]=
    {
        {1,"abdullah","0","Bapakos",},
        {2,"icih","0","Ibukos",},
        {3,"sueb","1","BudakKorporat"},
        {4,"anton","2","kangchiken",},
        {5,"avikadivi","3","Masikuliah",}
    };

  int idWargaKosYangHarusBebersihHalaman = 3;

  warga[1].nama = "ahmed";

  for (int i = 0; i < 5; i++) {

    if (warga[i].id == idWargaKosYangHarusBebersihHalaman) {
	    cout << "Ayo kamu harus melakukan piket " << warga[i].nama << " ayo cepatt \n";
	    break;
  		}
  	cout << "lihat itu si " << warga[i].nama << " kasian banget " << warga[i].pekerjaan << "\n";
	}	
}
```
## Penggunaan continue 

``` cpp 
#include<iostream>
using namespace std;

struct game_A{
    int id;
    string nama ;
    string skill;
    int buff;
};
int main (){
    int buffMaksimalCharacter = 150;
    
    game_A chara[] = 
        {
        {1,"Agumon"," Nafas api ", 30},
        {2,"Peemon"," Tinju super",35},
        {3,"BlackRyoumon"," Putaran Maut",40},
        {4,"Evolved Peemon"," Ultimate Laser peemon",210},
        {5,"Evolved Agumon"," Ultimate Rising fire Agumon",200},
        };
    
    for (int i = 0; i < 5; i++){
        if (chara[i].buff > buffMaksimalCharacter){
            continue;
        }
        cout<< " Congrats," << chara[i].nama << chara[i].skill << " you have buffed \n";
    }
}

```
