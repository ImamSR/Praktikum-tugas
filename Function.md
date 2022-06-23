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
