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
            title: Text('TabBar com widgets'),
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
              // Primeira aba com Builder para o SnackBar
              Container(
                child: Column(
                  mainAxisAlignment: MainAxisAlignment.center,
                  children: [
                    Text(
                      "Seja bem vindo(a)!",
                      style: TextStyle(fontSize: 20),
                    ),
                    SizedBox(height: 20),
                    Builder(
                      builder: (context) {
                        return ElevatedButton(
                          onPressed: () {
                            ScaffoldMessenger.of(context).showSnackBar(
                              SnackBar(
                                content: Text('Este é um SnackBar'),
                                duration: Duration(seconds: 2),
                                action: SnackBarAction(
                                  label: 'Desfazer',
                                  onPressed: () {
                                    ScaffoldMessenger.of(context).showSnackBar(
                                      SnackBar(content: Text('Ação desfeita')),
                                    );
                                  },
                                ),
                              ),
                            );
                          },
                          child: Text("Mostrar SnackBar"),
                        );
                      },
                    ),
                  ],
                ),
              ),


              // Segunda aba com imagem
              Image.network(
                'https://wallpapers.com/images/hd/pochacco-with-cinnamonroll-and-pompompurin-snhfo3ira7hu5kdu.jpg',
              ),


              // Terceira aba com lista de ícones
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



