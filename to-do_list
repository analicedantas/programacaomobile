

import 'package:flutter/material.dart';


void main() {
  runApp(MyApp());
}


class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: DefaultTabController(
        length: 3,
        child: Scaffold(
          appBar: AppBar(
            backgroundColor: Color.fromARGB(255, 255, 212, 226),
            title: Text('TabBar com Widgets'),
            bottom: TabBar(
              tabs: [
                Tab(
                  icon: Icon(Icons.home),
                  text: 'Início',
                ),
                Tab(
                  icon: Icon(Icons.image),
                  text: 'Imagem',
                ),
                Tab(
                  icon: Icon(Icons.star),
                  text: 'Ícones',
                ),
              ],
            ),
          ),
          body: TabBarView(
            children: [
              Container(
                child: Column(
                  mainAxisAlignment: MainAxisAlignment.center,
                  children: [
                    Text(
                      "Seja bem vindo(a)!",
                      style: TextStyle(fontSize: 20),
                    ),
                    SizedBox(height: 20),
                    ElevatedButton(
                      onPressed: () {},
                      child: Text("Clique aqui"),
                    ),
                  ],
                ),
              ),
              Image.asset('imagens/amigos.png'),
              ListView(
                children: [
                  ListTile(
                    leading: Icon(Icons.star, color: Colors.yellow),
                    title: Text('Fazer colagens'),
                  ),
                  ListTile(
                    leading: Icon(Icons.star, color: Colors.yellow),
                    title: Text('Estudar'),
                  ),
                  ListTile(
                    leading: Icon(Icons.star, color: Colors.yellow),
                    title: Text('Fazer um artigo'),
                  ),
                ],
              ),
            ],
          ),
        ),
      ),
    );
  }
}



