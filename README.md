# Trabalho1_Flutter

'''
//Questão 1

class Carro {
  String placa;
  String cor;
  String ano;

  Carro({
    required this.placa,
    required this.cor,
    required this.ano,
  });
}

void main() {
  Carro ferrari = Carro(
    placa: 'ABC1234',
    cor: 'preto',
    ano: '2021',
  );

  print(ferrari.placa);
  print(ferrari.cor);
  print(ferrari.ano);
}

//Questão 2

double calcProd(double a, double b) {
  double res = a * b;
  return res;
}

void main() {
  double res = calcProd(2.0, 4.0);
  print(res);
}

//Questão 3

class Carro {
  String placa;
  String cor;
  int ano;

  Carro(this.placa, this.cor, this.ano);
}

class CarroFrete extends Carro {
  double capacidade;

  CarroFrete(String placa, String cor, int ano, this.capacidade) : super(placa, cor, ano);
}

void main() {
  CarroFrete meuCarro = CarroFrete("ABC1234", "Prata", 2021, 2.5);
  print("Placa: ${meuCarro.placa}, Cor: ${meuCarro.cor}, Ano: ${meuCarro.ano}, Capacidade: ${meuCarro.capacidade}");
}

//Questão 4

void main() {

 for (int numero = 1; numero <= 100; numero++){
   if (numero % 2 == 0) {
     print("Valor de i = $numero -> par");
   } else{
     print("Valor de i = $numero");
   }
 }
}

//Questão 5

abstract class Aluno {
  int _matricula;
  String _nome;

  Aluno(this._matricula, this._nome);

  int getMatricula() => _matricula;

  String getNome() => _nome;

  double calcularMedia(List<double> notas) {
    double soma = 0.0;
    for (int i = 0; i < notas.length; i++) {
      soma += notas[i];
    }
    return soma / notas.length;
  }
}

class AlunoEspecial extends Aluno {
  int _limiteDisciplina;

  AlunoEspecial(int matricula, String nome, this._limiteDisciplina)
      : super(matricula, nome);

  int getLimiteDisciplina() => _limiteDisciplina;

  @override
  double calcularMedia(List<double> notas) {
    double soma = 0.0;
    double peso = 3.0;
    for (int i = 0; i < notas.length; i++) {
      soma += notas[i] * peso;
      peso -= 0.2;
      if (peso == 0) {
        break;
      }
    }
    double somaPesos = (3.0 + 2.8 + 2.6 + 2.4 + 2.2 + 2.0 + 1.8 + 1.6 + 1.4 + 1.2);
    return soma / somaPesos;
  }
}
void main() {
  AlunoEspecial aluno2 = AlunoEspecial(2, "Maria", 4);
  List<double> notasAluno2 = [7.0, 8.5, 9.2, 6.5, 8.0];
  double mediaAluno2 = aluno2.calcularMedia(notasAluno2);
  print("Aluno Especial: ${aluno2.getNome()} | Limite de disciplinas: ${aluno2.getLimiteDisciplina()} | Média: $mediaAluno2");
}

//Questão 6

abstract class Aluno {
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

class AlunoEspecial extends Aluno {
  int _limiteDisciplina;

  AlunoEspecial(int matricula, String nome, this._limiteDisciplina) : super(matricula, nome);

  int getLimiteDisciplina() => _limiteDisciplina;

  @override
  String toString() {
    return "AlunoEspecial{matricula: $_matricula, nome: $_nome, limiteDisciplina: $_limiteDisciplina}";
  }
}

void main() {
  AlunoEspecial aluno = AlunoEspecial(12345, "João", 5);
  print(aluno);
}

//Questão 7

class Ingresso {
  int dia;
  int mes;
  int ano;
  double valor;

  Ingresso(this.dia, this.mes, this.ano, this.valor);

  String toString() {
    return "$dia/$mes/$ano: ${valor.toStringAsFixed(2)}";
  }
}

void main() {
  List<Ingresso> ingressos = [
    Ingresso(11, 6, 2023, 35.20),
    Ingresso(15, 7, 2023, 25.50),
    Ingresso(22, 8, 2023, 18.00),
    Ingresso(5, 9, 2023, 42.00)
  ];

  for (int i = 0; i < ingressos.length; i++) {
    print(ingressos[i]);
  }
}

//Questão 8
class Carro {
  String _placa;
  String _modelo;
  int _ano;
  Carro(this._placa, this._modelo, this._ano);
  String getPlaca() => _placa;
  String getModelo() => _modelo;
  int getAno() => _ano;
  @override
  String toString() {
    return "Placa: $_placa \nModelo: $_modelo \nAno: $_ano";
  }
}
  void main() {
    // criação dos objetos Carro
    Carro carro1 = Carro("ABC1234", "Gol", 2010);
    Carro carro2 = Carro("DEF5678", "Celta", 2018);
    Carro carro3 = Carro("JKK0102", "Palio", 2015);
    Carro carro4 = Carro("BTR2345", "Uno", 2012);

    // criação do Map e adição dos objetos
    Map<String, Carro> carros = {
      carro1.getPlaca(): carro1,
      carro2.getPlaca(): carro2,
      carro3.getPlaca(): carro3,
      carro4.getPlaca(): carro4,
    };

    // percorrendo o Map e exibindo os dados dos carros na tela
    for (Carro carro in carros.values) {
      print(carro);
      print("------");
    }
  }


'''

