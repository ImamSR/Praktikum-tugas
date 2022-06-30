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

void intro();
void controller();
void pemilihanNaga();

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

dragonoid constructor(string name, string type, string skill, int lvl){
	dragonoid dragon;
	dragon.nama = name;
	dragon.skill = skill;
	dragon.tipe = type;
	dragon.lvl = lvl;
	return dragon;
}

void feedDragon(dragonoid*dg){
	dg->lvl = dg->lvl+10 ;
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
	dragonoid dragon1;
	dragon1 = constructor("Pure Flame Dragon","Fire","Basic Fire Attack",25);
	
	dragonoid dragon2;
	dragon2 = constructor("Gummon Dragon","Nature","Basic Root Attack",30);
	
	dragonoid dragon3;
	dragon3 = constructor("Orsted Dragon evolved", "Light Dragon", "Ultimate Light Attack",35);

	dragonoid dragon4;
	dragon4 = constructor("Dirra Dragon Evolved","Angel Dragon", "Judgement Dirra", 40);
	 
	dragonoid dragon5;
	dragon5 = constructor("Lerx Dragon Freak"," Ultimate Dragonoid "," Ultimate Lerx Dragon",45 );
	 
	dragonoid dragon6;
	dragon6 = constructor("Frost Dragon Evolved","Ice Dragon","Frost Dragon Breath", 50 );

    cout << " Pilih naga yang ingin di beri makan\n"
			" 1.Pure Flame Dragon\n"
			" 2.Gummon Dragon\n"
			" 3.Orsted Dragon\n"
			" 4.Dirra Dragon\n"
			" 5.Lerx Dragon\n"
			" 6.Frost Dragon\n" 
			" \nPilih : ";
    cin >> naga;
	
	if (naga == 1 ){
		cout << "Level saat ini "<< dragon1.lvl << endl;
		feedDragon(&dragon1);
        cout <<"Lvl Up !!\n"<<dragon1.nama << endl <<"Selamat Anda telah menaikan naga anda "<< dragon1.lvl << endl;
        dragonoid*dragon1;
    }
    if (naga == 2 ){
    	cout <<"Level Saat ini "<< dragon2.lvl << endl;
    	feedDragon(&dragon2);
        cout << "Lvl up !!\n " <<dragon2.nama << endl <<" Selamat anda menaikan Level naga anda menjadi "<< dragon2.lvl << endl;
    }
    if (naga == 3 ){
    	cout <<"Level saat ini "<< dragon3.lvl << endl;
    	feedDragon(&dragon3);
        cout << "Lvl up !!\n " <<dragon3.nama << endl <<"Selamat anda menaikan level anda menjadi "<< dragon3.lvl << endl;
    }
    if (naga == 4 ){
    	cout << "Level saat ini" << dragon4.lvl << endl;
    	feedDragon(&dragon4);
        cout << "Lvl Up !!\n " <<dragon4.nama << endl <<" Selamat Naga Anda Naik Level menjadi  " << dragon4.lvl <<endl;
    }
    if (naga == 5){
    	cout << "Level saat ini " << dragon5.lvl << endl;
    	feedDragon(&dragon5);
        cout << "Lvl Up !!\n " <<dragon5.nama << endl <<" Selamat naga anda naik level menjadi " << dragon5.lvl << endl;
    }
    if (naga == 6){
    	cout << " Level saat ini " << dragon6.lvl << endl;
    	feedDragon(&dragon6);
        cout << "Lvl Up !!\n " <<dragon6.nama << endl <<" Selamat Naga Ultimate anda Naik level menjadi  " << dragon6.lvl << endl;
    }
}

void intro(){
    string kisah;
    cout << "=====================================================\n" << endl;
    cout << "         Selamat Datang di Game Dragon City         \n" << endl;
    cout << "=====================================================\n\n\n" << endl;

    cout << "Input Apa Saja Untuk Melanjutkan" << endl;
    cin >> kisah;
    system("cls");

    cout << "==============================================================\n\n\n";
    cout << "Disuatu Tempat Dimana Berkumpulnya Para Naga Untuk Mencari Makan " << endl;
    cout << "Namun Ada Seseorang Yang Menjinakan Semua Naga Nya Itu Untuk"<< endl;
    cout << "Budidaya Naga Namun Naga Naga Sangat Rakus Dalam Hal Makanan " << endl;
    cout << "Ikuti Game nya\n\n"<< endl;
    cout << "==============================================================\n\n" << endl;

    cout << "Input Apa Saja Untuk Melanjutkan Ke Dalam Game" << endl;
    cin >> kisah;
    system("cls");
}

int main(){
	intro();
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
			peta[posisiKarakterY][posisiKarakterX] = " ";
    }
    if ((peta[posisiKarakterY][posisiKarakterX] == "G")){
			pemilihanNaga();
    }
    if ((peta[posisiKarakterY][posisiKarakterX] == "O")){
    		pemilihanNaga();
    		peta[posisiKarakterY][posisiKarakterX] = " ";
    }
    if ((peta[posisiKarakterY][posisiKarakterX] == "D")){
        	pemilihanNaga();
        	peta[posisiKarakterY][posisiKarakterX] = " ";
    }
    if ((peta[posisiKarakterY][posisiKarakterX] == "L")){
    		pemilihanNaga();
    		peta[posisiKarakterY][posisiKarakterX] = " ";
    }
	if ((peta[posisiKarakterY][posisiKarakterX] == "F")){
			pemilihanNaga();
			peta[posisiKarakterY][posisiKarakterX] = " ";
		}
	arrowKey = _getch();
	controller();
    }
    cin.get();
    return 0;
}
```
