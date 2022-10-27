# Jokenpo
Simples iniciante. Beginner.

import java.util.Scanner;
import java.util.Random;

public class Main {
  public static void main(String[] args) {
    System.out.println("");
    System.out.println("Digite 1 para PAPEL");
    System.out.println("Digite 2 para PEDRA");
    System.out.println("Digite 3 para TESOURA");
    System.out.println("");

    Scanner leitor = new Scanner(System.in);
    Random gerador = new Random();
    int numeroUsuario;
    int escolhaComputador;
    int pontosUsuarios = 0;
    int pontosComputador = 0;

    for (int i = 0; i < 5; i++){
      numeroUsuario = leitor.nextInt();
      escolhaComputador = gerador.nextInt(3) + 1;
      // verificaescolha computador
      switch(escolhaComputador){
        case 1:
          System.out.println("Computador escolheu PAPEL");
          break;
        case 2:
          System.out.println("Computador escolheu PEDRA");
          break;
        case 3:
          System.out.println("Computador escolheu TESOURA");
          break;
      }
      //verificação resultado
      if(numeroUsuario > 3 || numeroUsuario <=0){
        System.out.println("INVALIDO");
      }
      if(numeroUsuario == escolhaComputador){
        System.out.println("EMPATE");
      }
      else if((numeroUsuario - escolhaComputador) == -1 || (numeroUsuario - escolhaComputador) == 2) {
      System.out.println("USUARIO VENCEU PARTIDA");
        pontosUsuarios++;
      }
      else {
        System.out.println("COMPUTADOR VENCEDOR PARTIDA");
        pontosComputador++;
      }
      } //acaba o laço
    System.out.println("");
    if(pontosUsuarios > pontosComputador){
      System.out.println("USUARIO GANHOU O JOGO");
    }
    else if(pontosUsuarios < pontosComputador){
      System.out.println("COMPUTADOR GANHOU O JOGO");
    }
    else {
      System.out.println("EMPATE");
    }
    }
}
