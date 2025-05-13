import 'package:flutter/material.dart'; // Importa o pacote Flutter Material, que contém widgets e temas para a interface.


void main(){
  runApp(MyApp());
}


class MyApp extends StatelessWidget{
  @override
 
  Widget build(BuildContext context){
    return MaterialApp(
      title: 'Calcular média',
      theme: ThemeData(primaryColor:Colors.purple),
      home: CalcularMedia(),
    );
  }
}
class CalcularMedia extends StatefulWidget{
  @override


  _CalcularMediaState createState() => _CalcularMediaState();


}


class _CalcularMediaState extends State<CalcularMedia>{
  final TextEditingController _nota1Controller = TextEditingController();
  final TextEditingController _nota2Controller = TextEditingController();


  double? _media;


  void _calcularMedia(){
    final double nota1 = double.tryParse(_nota1Controller.text)??0;
    final double nota2 = double.tryParse(_nota2Controller.text)?? 0;


    if(nota1 > 0 && nota2 > 0){
      setState((){
        _media = (nota1+nota2)/2;


      });
     
    }
  }


@override


Widget build(BuildContext context){
  return Scaffold(
    appBar: AppBar(
      title:Text("Calcular a média bimestral do aluno"),
      backgroundColor: Colors.purple,
    ),
    body: Padding(
      padding: const EdgeInsets.all(18.0),
      child: Column(
        children:[
          TextField(
            controller: _nota1Controller,
            decoration: InputDecoration(
              labelText: "Primeira nota",
            ),
          ),
          TextField(
            controller: _nota2Controller,
            decoration: InputDecoration(
              labelText: "Segunda nota",
            ),
          ),
          SizedBox(
            height: 20,
          ),
          ElevatedButton(
            onPressed: _calcularMedia,
            child: Text("Calcular a média bimestral"),
          ),
          SizedBox(
            height: 20,
          ),
          if(_media != null)
          Text ('Sua média nesse bimestre foi igual a ${_media!.toStringAsFixed(2)}',
          style: TextStyle(fontSize: 15),
          ),
        ],
      ),
    ),
  );
}
}
