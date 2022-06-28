## Game Dragon city 

```cpp
#include<iostream>
#include<conio.h>
#include<string.h>
#include<windows.h>
#include<stdio.h>
using namespace std;

struct dragonoid{
    string nama;
    string tipe;
    string skill;
    int lvl;
};
struct Makanan{
	string nama;
	string tipe;
	int LvlUp;
};

const int panjangPeta = 20;
const int lebarPeta = 16;

char arrowKey;
int posisiKarakterY = 15;
int posisiKarakterX = 10;

void controller();
void pemilihanNaga();
void feed();


string peta[lebarPeta][panjangPeta] = {
        {"=","=","=","=","=","=","=","=","=","=","=","=","=","=","=","=","=","=","=","="},
        {"="," "," "," ","="," "," "," "," "," "," "," "," "," ","="," "," "," ","F","="},
        {"=","L"," "," "," "," ","="," ","=","=","="," ","="," ","="," "," "," "," ","="},
        {"=","=","=","=","="," ","="," "," ","P"," "," ","="," ","="," ","=","=","=","="},
        {"="," "," "," "," "," ","=","=","=","=","=","=","="," "," "," "," "," "," ","="},
        {"=","=","="," ","="," "," "," "," "," "," "," "," "," "," ","="," ","=","=","="},
        {"="," "," "," ","="," "," "," "," "," "," "," "," "," "," ","="," "," "," ","="},
        {"="," "," "," ","="," "," "," "," "," "," "," "," "," "," ","="," "," "," ","="},
        {"="," "," "," ","="," "," "," "," "," "," "," "," "," "," ","="," "," "," ","="},
        {"=","=","=","=","="," "," "," "," "," "," "," "," "," "," ","=","=","=","=","="},
        {"="," "," "," "," "," "," "," "," "," "," "," "," "," "," "," "," "," "," ","="},
        {"="," ","=","=","#","#","#"," ","#","#","#","#"," ","#","#","#","=","="," ","="},
        {"="," "," ","=","#","#","#"," ","#","#","#","#"," ","#","#","#","="," "," ","="},
        {"="," "," ","=","#","#","#"," ","#","#","#","#"," ","#","#","#","="," "," ","="},
        {"=","O"," ","="," "," "," "," "," "," "," "," "," "," "," "," ","="," ","D","="},
        {"=","=","=","=","=","=","=","="," "," "," "," ","=","=","=","=","=","=","=","="},
        };

int main(){
    while(1){
	system ("cls");
    for(int y=0; y<lebarPeta; y++) {
        for(int x=0; x<panjangPeta; x++) {       
            if(posisiKarakterX == x && posisiKarakterY == y) {
                cout << "C" << " ";
            } 
            else{
            cout << peta[y][x] << " ";
            }
        }
        cout << "\n";
    }    
    if (peta[posisiKarakterY][posisiKarakterX] == "P"){
			pemilihanNaga();
    }
    if ((peta[posisiKarakterY][posisiKarakterX] == "G")){
			pemilihanNaga();
    }
    if ((peta[posisiKarakterY][posisiKarakterX] == "O")){
    		pemilihanNaga();
    }
    if ((peta[posisiKarakterY][posisiKarakterX] == "D")){
        	pemilihanNaga();
    }
    if ((peta[posisiKarakterY][posisiKarakterX] == "L")){
    		pemilihanNaga();
    }
	if ((peta[posisiKarakterY][posisiKarakterX] == "F")){
			pemilihanNaga();
		}
	arrowKey = _getch();
	controller();
    }
    cin.get();
    return 0;
}


void controller() {
    if ((arrowKey == 'w') && (peta[posisiKarakterY - 1][posisiKarakterX] != "=" && peta[posisiKarakterY - 1][posisiKarakterX] != "#" && posisiKarakterY >= 1)) {
        // Gerakkan karakter ke atas
        posisiKarakterY = posisiKarakterY - 1;
    }
    if ((arrowKey == 's') && (peta[posisiKarakterY + 1][posisiKarakterX] != "=" && peta[posisiKarakterY + 1][posisiKarakterX] != "#" && posisiKarakterY < lebarPeta - 1)) {
        // Gerakkan karakter ke atas
        posisiKarakterY = posisiKarakterY + 1;
    }
    if ((arrowKey == 'a') && (peta[posisiKarakterY][posisiKarakterX - 1] != "=" && peta[posisiKarakterY][posisiKarakterX - 1] != "#" && posisiKarakterX >= 0)) {
        // Gerakkan karakter ke atas
        posisiKarakterX = posisiKarakterX - 1;
    }
    if ((arrowKey == 'd') && (peta[posisiKarakterY][posisiKarakterX + 1] != "=" && peta[posisiKarakterY][posisiKarakterX + 1] != "#" && posisiKarakterX < panjangPeta - 1)) {
        // Gerakkan karakter ke atas
        posisiKarakterX = posisiKarakterX + 1;
    }
    if (arrowKey == 'x') {
        exit(0);
    }
}
void pemilihanNaga(){
    int naga;
    int makanan;
	dragonoid dragon1;
	dragon1.nama = " Pure Flame Dragon ";
	dragon1.tipe = " Api";
	dragon1.skill= " Basic fire breath"; 
	dragon1.lvl	 = 25;
	
	dragonoid dragon2;
	dragon2.nama = "Gummon dragon";
	dragon2.tipe = "Nature";
	dragon2.skill= "Basic root attack"; 
	dragon2.lvl	 = 30;
	
	dragonoid dragon3;
	dragon3.nama = "Orsted Dragon Evolved";
	dragon3.tipe = "Light";
	dragon3.skill= "Ultimate Light Attack";
	dragon3.lvl	 = 35;
	 
	dragonoid dragon4;
	dragon4.nama = "Dirra Dragon Evolved";
	dragon4.tipe = "Angel Dragon ";
	dragon4.skill= "Judgement Dirra";
	dragon4.lvl	 = 40;
	 
	dragonoid dragon5;
	dragon5.nama = "Lerx Dragon Freak";
	dragon5.tipe = "Ultimate Dragonoid";
	dragon5.skill= "Ultimate Lerx Judgement";
	dragon5.lvl	 = 45;
	 
	dragonoid dragon6;
	dragon6.nama = "Frost Dragon Evolved";
	dragon6.tipe = "Frost dragon";
	dragon6.skill = " Frost Breath ";
	dragon6.lvl = 50;

    cout << " Pilih naga yang ingin di beri makan\n"
			" 1. Pure Flame Dragon\n"
			" 2. Gummon Dragonn\n"
			" 3. Orsted Dragon\n"
			" 4. Dirra Dragon\n"
			" 5. Lerx Dragon\n"
			" 6. Frost Dragon\n" 
			" \nPilih : ";
    cin >> naga;
	
	if (naga == 1 ){
        cout << "Lvl Up !!\n" <<dragon1.nama << endl <<"Feed me I`m hungry" << endl;
        
        do{
        	cout << "makanan ";
        	cin>> makanan;
        	
        	swith 
		}
    }
    if (naga == 2 ){
        cout << "Lvl up !!\n " <<dragon2.nama << endl <<" Feed me I`m still a litle dragon" << endl;
    }
    if (naga == 3 ){
        cout << "Lvl up !!\n " <<dragon3.nama << endl <<" Feed me for Lvl up" << endl;
    }
    if (naga == 4 ){
        cout << "Lvl Up !!\n " <<dragon4.nama << endl <<" Feed me Master" << endl;
    }
    if (naga == 5){
        cout << "Lvl Up !!\n " <<dragon5.nama << endl <<" Feed me BABU!!" <<endl;
    }
    if (naga == 6){
        cout << "Lvl Up !!\n " <<dragon6.nama << endl <<" Sssssss " <<endl;
    }
    
    
}
```
