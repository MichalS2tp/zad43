#include <stream>
#include <cstring>
#include <iostream>
#include <string>
#include <fstream>

using namespace std;

class a{
       ifstream plik1;
       ofstream plik2;
       string start[1000];
       string sort[1000];

  public:
        a();
        ~a();
       
        void wczytaj();     
		string stringSort(string s);  
};

    a::a(){ 
    plik1.open("c:\\1.txt");
    plik2.open("c:\\2.txt");
}

void a::a(){
	
	string v3;
	int x1;
	int i=0;
	
	plik2<<"[";
	
	while(!plik1.eof()){ 
        plik1>>v3;
        
    orginal[i]=v3;
		sort[i]=stringSort(v3);
		i++;
	}
	
	for(int j=0;j<i;j++){
		if(sort[j]==sort[j+1]){
			plik2<<"{\"program"<<"\":\""<<start[j]<<"\",\"anagram\":\""<<start[j+1]<<"\"},";
		}
	}
	
	plik2<<"]";

}

string a::stringSort(string){
	
	int t[150]; 
	string wynik;
	
	
	for (int i=0; i<=150; i++)
        t[i]=0;

   
    for (int i=0; i<=s.length()-1; i++)
    {
        t[i]=(int)s[i];
    }

    int l[256]; 

  
    for (int i=0; i<=150; i++)
        l[i]=0;

    for (int i=0; i<=150; i++){
    	l[t[i]]++;

	}
    for (int i=0; i<=255; i++)
    {
        if (l[i]>0)
           for (int j=1; j<=l[i]; j++)
           if(i>0)
           wynik+=(char)i;
            }
	
	
	return wynik;
	
}

    a::~a(){
    plik1.close();
    plik2.close();
}



int main(int argc, char** argv) {
	
	  a a1; 
    a1.wczytaj(); 
    
    return 0;
	}
