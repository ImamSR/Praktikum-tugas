## Total Beli 

```cpp
#include <iostream>
using namespace std;

void hitungHarga(int hargaSatuan, int jumlahBeli, int diskon) {
    
    int totalHarga=hargaSatuan*jumlahBeli;
    int totalDiskon = totalHarga*diskon/100;
    int totalHargaKurangDiskon=totalHarga-totalDiskon;
    
    cout << "Total harga setelah diskon : " << totalHargaKurangDiskon;
}

int main() {
    
    int tahubulat, hargaTahubulat;
    
    cout<<"Harga Tahu bulat satuan: ";
    cin>>hargaTahubulat;
    
    cout<<"Jumlah Tahu bulat yang dibeli: ";
	cin>>tahubulat;
	
	hitungHarga(hargaTahubulat, tahubulat, 5);

    return 0;
}
```
## Nilai Akhir 

```cpp
include<iostream>
using namespace std;

void nilaiA(int nilaiMax){

string index;

if (nilaiMax >=100){
	index = "SSR";
}else if (nilaiMax > 90){
	index = "SS";
}else if (nilaiMax > 80){
	index = "S";
}else if (nilaiMax > 70){
	index = "A";
}else if (nilaiMax > 65){
	index = "B";
}

cout<<"Nilai yang kamu miliki : "<< nilaiMax  <<"\nMaka Grade kamu : "<< index;
}
int main () {
	int Nilai;
	cout<<"Masukan Nilai :";
	cin>>Nilai;
	
	nilaiA(Nilai);
	
	return 0;
}
```
## Tambahan 

```cpp
#include<iostream>
using namespace std;

void ulang();
void Ppanjang(){
	int panjang; int lebar; int luasPersegiPanjang;
	cout<<"Panjang : ";
	cin>>panjang;
	cout<<"Lebar : ";
	cin>>lebar;
	luasPersegiPanjang=panjang*lebar;
	cout<<"Luas persegi panjang :"<<luasPersegiPanjang<<"\n\n";
	ulang();
}
void lingkaran(){
	int jarijari;
	float KelilingLingkaran;
	cout<<"Jari-jari : ";
	cin>>jarijari;
	KelilingLingkaran=2*3.14*jarijari;
	cout<<"Keliling Lingkaran : "<<KelilingLingkaran<<"\n\n";
	ulang();
}

void segitiga(){
	int alas; int tinggi;
	float luasSegitiga; 
	cout<<"Alas :";
	cin>>alas;
	cout<<"Tinggi :";
	cin>>tinggi;
	luasSegitiga=0.5*alas*tinggi;
	cout<<"Luas segitiga :"<<luasSegitiga<<"\n\n";
	ulang();
}
int main(){
	int pilihan;
	cout<<	"Pilihan Rumus \n"
			"1. luas persegi pannjang \n"
			"2. Keliling Lingkaran\n"
			"3. Luas Segitiga\n";
	cout<<"Masukan Pilihan :\n";
	cin>>pilihan;
	switch(pilihan){
		case 1:
			Ppanjang();
			break;
		case 2:
			lingkaran();
			break;
		case 3:
			segitiga();
			break;
	}
}

void ulang(){
	int ulang;
	cout<<"Apakah anda ingin mencoba rumus yang lain? \n"
			"1. Ya \n"
			"2. Tidak \n";
	cout<<"Masukan pilihan :";
	cin>>ulang;
	
	switch (ulang){
		case 1:
			main();
			break;
		case 2:
			cout<<"Terimakasih, Arigatou gozaimasu!";
			break;
	}
	
}
```
