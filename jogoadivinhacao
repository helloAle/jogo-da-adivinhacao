#include<iostream>
#include<stdlib.h>
#include<cstdlib>
#include<ctime>
using namespace std;

int main ()
{
	cout << "\n\n  **************************************" << endl;
	cout << "  * Bem-vindos ao jogo da adivinhacao! *" << endl;
	cout << "  **************************************\n\n" << endl;
	
	cout << " Escolha o seu nivel de dificuldade: " << endl;
	cout << "  Facil (F), Medio (M), Dificil (D)" << endl;
	
	char dificuldade;
	cin >> dificuldade;
	
	int numero_de_tentativas;
	
	if(dificuldade=='F', 'f'){
		numero_de_tentativas = 15;
	}
	else if(dificuldade=='M', 'm'){
		numero_de_tentativas = 10;
	}
	else{
		numero_de_tentativas = 5;
	}
	
	srand(time(NULL));
	const int SN = rand() % 100;
	
	bool na = true;
	int tentativas = 0;
	
	double pontos = 1000.0;
	
	for(tentativas = 1; tentativas <= numero_de_tentativas; tentativas++){
		int chute;
		cout << " Tentativa " << tentativas << endl;
	    cout << " Qual seu chute?\n..............";
	    cin >> chute;
	    
	    double pp = abs(chute - SN)/2.0;
	    pontos = pontos - pp;
	
	    cout << "\n O valor do seu chute foi: " << chute << endl;
	    bool acertou = chute == SN;
	    bool maior = chute > SN;
	
	    if(acertou)
		{
	    	cout << " Parabens, voce acertou o numero secreto!" << endl;
	    	na = false;
	    	break;
    	}
    	else if(maior)
		{
	    	cout << " Seu chute foi maior que o numero secreto" << endl;
    	}
    	else
		{
	    	cout << " Seu numero foi menor que o numero secreto" << endl;
    	}
	}
	cout << " Fim de jogo!\n";
	if(na){
		cout << "Voce perdeu, tente novamente!" << endl;
	}
	else{
    	cout << " Voce acertou em " << tentativas << " tentativas!" << endl;
    	cout .precision(2);
	    cout << fixed;
	    cout << " Sua pontucao foi de " << pontos << " pontos!" << endl;
    }
}
