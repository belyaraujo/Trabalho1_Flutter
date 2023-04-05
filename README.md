# Trabalho1_Flutter

//Quetão 1

// class Carro{
//   String placa;
//   String cor;
//   String ano;
  
//   Carro({
//     required this.placa,
//     required this.cor,
//     required this.ano,
//   });
// }

// void main() {
//   Carro ferrari = Carro(
//   placa: 'ABC1234',
//   cor: 'preto',
//   ano: '2021',
//   );
  
//   print(ferrari.placa);
//   print(ferrari.cor);
//   print(ferrari.ano);
// }

//Quetão 2

// double calcProd(double a, double b) {
// double res = a * b;
// return res;
// }

// void main() {
//  double res = calcProd(2.0, 4.0);
//   print(res);
// }

//Questão 3

// class Carro{
//   String placa;
//   String cor;
//   String ano;
  
//   Carro({
//     required this.placa,
//     required this.cor,
//     required this.ano,
//   });
  
  
// }

// void main() {
//   Carro ferrari = Carro(
//   placa: 'ABC1234',
//   cor: 'preto',
//   ano: '2021',
//   );
  
 // Questão 4

// void main() {
  
//   for (int numero = 1; numero <= 100; numero++){
//     if (numero % 2 == 0) {
//       print("Valor de i = $numero -> par");
//     } else{
//       print("Valor de i = $numero");
//     }
//   }
// }

//Questão 5

abstract class Aluno{
int _matricula;
String _nome;
Aluno(this._matricula,this._nome);
int getMatricula() => _matricula;
String getNome() => _nome;
double calcularMedia(List notas){
double soma = 0.0;
for(int i = 0; i < notas.length; i++){
soma += notas[i];
}
return soma/notas.length;
}
}
class AlunoEspecial extends Aluno{
int _limiteDisciplina;
AlunoEspecial(int matricula, String nome,this._limiteDisciplina):super(matricula,nome);
int getLimiteDisciplina() =>_limiteDisciplina;
}


