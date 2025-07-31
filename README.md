import 'package:flutter/material.dart';

void main() => runApp(MaterialApp(home: MyLayout()));

class MyLayout extends StatefulWidget {
  @override
  _MyLayoutState createState() => _MyLayoutState();
}

class _MyLayoutState extends State<MyLayout> {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Layout Manager Example'),
      ),
      body: Column(
        children: [
          Row(
            children: [
              Expanded(
                child: Container(
                  height: 50,
                  color: Colors.red,
                ),
              ),
              SizedBox(width: 8),
              Expanded(
                child: Container(
                  height: 50,
                  color: Colors.green,
                ),
              ),
              SizedBox(width: 8),
              Expanded(
                child: Container(
                  height: 50,
                  color: Colors.blue,
                ),
              ),
            ],
          ),
          SizedBox(height: 16),
          Container(
            height: 50,
            color: Colors.orange,
          ),
          SizedBox(height: 10),
          Expanded(
            child: ListView(
              children: List.generate(
                3,
                (i) => Container(
                  height: 50,
                  margin: EdgeInsets.symmetric(vertical: 4, horizontal: 8),
                  decoration: BoxDecoration(
                    border: Border.all(color: Colors.grey[300]!),
                  ),
                  child: Center(
                    child: Text('Item ${i + 1}'),
                  ),
                ),
              ),

            ),
          ),
        ],
      ),
    );
  }
}
