## Cuaderno
Aqui podremos ver mis notas 

## PRIMER PROGRAMA
```

# sub cuaderno
  msgbox "hola sena" 
  msgbox "hola mundo"
# and sub

```

## 26 de agosto 20222

### CONDICIONAL SI 

```

Sub impuesto()
    a = Int(InputBox("valor a pagar anual"))
    
    If a > 0 And a < 1000 Then
       MsgBox " no pagar impuesto"
       
    Else
      If a > 1001 And 10000 Then
        ip = 0.05
        Total = a * ip
        
        MsgBox " el total es: " & Total
        
      Else
         If a > 10001 And a < 100000 Then
           ip = 0.1
           Total = a * ip
           
           MsgBox " el total es: " & Total
           
         Else
            If a > 100001 And a < 1000000 Then
                ip = 0.15
                Total = a * ip
                
                MsgBox " el total es: " & Total
              
            Else
                If a > 1000001 And a < 10000000 Then
                   ip = 0.2
                   Total = a * ip
                   
                   MsgBox " el total es: " & Total
                     
                Else
                  If a > 10000001 Then
                    ip = 0.25
                    Total = a * ip
                   
                   MsgBox " el total es: " & Total
                  
                  End If
                End If
            End If
          End If
       End If
    End If
End Sub

```
## 26 de agosto 2022

## CASO

```

Sub impuestos()
 
 a = Int(InputBox("ingreso anual"))
  
  Select Case a
     
     Case 0 To 1000:
      
         MsgBox "no paga impuesto"
      
     Case 1001 To 10000:
     
         Total = a * 0.05
      
     Case 10001 To 100000:
      
         Total = a * 0.1
     
     Case 100001 To 1000000:
     
         Total = a * 0.15
      
     Case 1000001 To 10000000:
     
         Total = a * 0.2
      
     Case 10000001:
      
         Total = a * 0.25
     
  End Select

 MsgBox "el total es: " & Total

End Sub

```

## 29 de agosto 2022

## FOR 

```

Sub nombre()
 
 fila = 4
 
 For n = 1 To 15
    nomb = InputBox("ingrese un nombre")
    Hoja1.Cells(fila, 2) = nomb
    fila = fila + 1
 Next n
 
End Sub

```

## 2 de septiembre 2022

## FOR (2)

```

Sub recolecta()
 tr = total_recaudado
 sb = si_abono
 nb = no_abono
 a = abono
 vs = valor_superior
 
 For e = 1 To 3
  a = Int(InputBox("ingrese una cantidad"))
    If a >= 1000 Then
        sb = sb + 1
      If a >= 10000 Then
        vs = vs + 1
      End If
    Else
      nb = nb + 1
    End If
    
  tr = tr + a
 
 Next e
 
 promedio = tr / sb
 MsgBox "si abono: " & sb
 MsgBox "no abono: " & nb
 MsgBox "abono mas de 10mil: " & vs
 MsgBox "total: " & tr
 MsgBox "promedio: " & promedio
 
End Sub

```

## 02 de septiembre 2022


## FOR (3)

```

Sub lista()

  For p = 2 To 21
     nomb = Hoja1.Cells(p, 1)
     ult = Len(nomb) - 1
     Hoja1.Cells(p, 2) = Mid(nomb, ult, 2)
  Next p
  
End Sub

```

## 02 de septiembre 2022


### FOR (4)

```
Sub lista 

 for p = 2 to 21 
  an = Hoja1.cells(p, 2)
  mp = Hoja1.cells(p, 3) 
  nomb = Hoja1.cells(p, 1)
  ult = len (mp) - 1 
  Hoja1.cells(p, 4) = Mid (an, 1, 2) + Mid (mp, ult, 2) + Mid (nomb, 1, 2)
 next p 

End sub
```

## 21 de septiembre 2022

### CICLO MQ (1)

```
Sub recolecta()
 tr = 0
 sb = 0
 nb = 0
 a = 0
 vs = 0
 
 While tr <= 3000000
   a = Int(InputBox("ingrese una cantidad"))
     If a > 0 Then
          sb = sb + 1
       If a >= 10000 Then
          vs = vs + 1
       End If
     Else
          nb = nb + 1
     End If
     
 Wend
 
 tr = tr + a
 promedio = tr / sb
 MsgBox "si abono: " & sb
 MsgBox "no abono: " & nb
 MsgBox "abono mas de 10mil: " & vs
 MsgBox "total: " & tr
 MsgBox "promedio: " & promedio
 
 
End Sub
```

## 14 de septiembre 2022

### CICLO MQ (2)

```
Sub datos()
    f = 1
    sw = True
    
    c = Int(InputBox("ingrese numero de cedula"))
    
    While sw
        If c = Hoja1.Cells(f, 2) Then
            n = Hoja1.Cells(f, 1)
            sw = False
            MsgBox "Su nombre es: " & n
        Else
            MsgBox "numero de documento no registrado"
            sw = False
            f = f + 1
        End If
    Wend
    
End Sub
```
## 23 de septiembre 2022

### Formulario Visual Basic

## Boton Buscar
```
Private Sub btnbc_Click()
    fila = registro.Cells(1, 6)
    sw = True
    
    txtcedu.Text = Int(InputBox("ingrese numero de cedula"))
    
    While sw
        If txtcedu.Text = registro.Cells(fila, 3) Then
            txtnomb.Text = registro.Cells(fila, 1)
            txtape.Text = registro.Cells(fila, 2)
            txttel.Text = registro.Cells(fila, 4)
            sw = False
        Else
            MsgBox "numero de documento no registrado"
            sw = False
        End If
        txtnomb.Enabled = False
        txtcedu.Enabled = False
        txtape.Enabled = False
        txttel.Enabled = False
    Wend
    fila = fila + 1
End Sub
```
## Boton Editar
```
Private Sub btnedt_Click()
    fila = registro.Cells(1, 6)
    sw = True
    
    txtcedu.Text = Int(InputBox("ingrese numero de documento"))
    
    While sw
      If txtcedu.Text = registro.Cells(fila, 3) Then
         txtnomb.Text = registro.Cells(fila, 1)
         txtape.Text = registro.Cells(fila, 2)
         txttel.Text = registro.Cells(fila, 4)
         sw = False
       Else
        MsgBox "numero de documento no registrado"
        sw = False
       End If
       fila = fila + 1
       txtcedu.Enabled = True
       txtnomb.Enabled = True
       txtape.Enabled = True
       txttel.Enabled = True
    Wend
End Sub
```
## Boton Guardar
```
Private Sub btngr_Click()
    fila = registro.Cells(1, 6)
    registro.Cells(fila, 1) = txtnomb.Text
    registro.Cells(fila, 2) = txtape.Text
    registro.Cells(fila, 3) = txtcedu.Text
    registro.Cells(fila, 4) = txttel.Text
    
    MsgBox "informacion registrada"
    
    txtnomb.Text = Empty
    txtape.Text = Empty
    txtcedu.Text = Empty
    txttel.Text = Empty
    btnnv.Enabled = True
    btngr.Enabled = False
    btnbc.Enabled = True
    btnedt.Enabled = True
    btnelm.Enabled = True
    txtnomb.Enabled = False
    txtape.Enabled = False
    txtcedu.Enabled = False
    txttel.Enabled = False
End Sub
```
```
Private Sub btnnv_Click()
    txtnomb.Enabled = True
    txtape.Enabled = True
    txtcedu.Enabled = True
    txttel.Enabled = True
    frmregistro.Caption = "registrando"
    
    btnnv.Enabled = False
    btngr.Enabled = True
    btnbc.Enabled = False
    btnedt.Enabled = False
    btnelm.Enabled = False
    txtnomb.SetFocus
    registro.Cells(1, 6) = registro.Cells(1, 6) + 1
End Sub
```
## Ventana de Eliminar
```
Private Sub btnelm_Click()
    frmeli.Show
    
End Sub

```
## Boton Eliminar
```
Private Sub UserForm_Click()

End Sub
Private Sub btnap_Click()
  registro.Rows(registro.Cells(1, 6)).EntireRow.Delete
  registro.Cells(1, 6) = registro.Cells(1, 6) - 1
  txtnomb.Text = ""
  txtape.Text = ""
  txtcedu.Text = ""
  txttel.Text = ""
  MsgBox "los datos se eliminaron"
End Sub
```
```
Private Sub btneli_Click()
  fila = registro.Cells(1, 6)
    sw = True
    
    txtcedu.Text = Int(InputBox("ingrese numero de documento"))
    
    While sw
      If txtcedu.Text = registro.Cells(fila, 3) Then
         txtnomb.Text = registro.Cells(fila, 1)
         txtape.Text = registro.Cells(fila, 2)
         txttel.Text = registro.Cells(fila, 4)
         sw = False
       Else
        MsgBox "numero de documento no registrado"
        sw = False
       End If
       fila = fila + 1
    Wend
End Sub
```

## 28 de septiembre 2022

### DART, OBJETOS, CLASES Y METODOS

```
void main() {
 
  Operacion operacion = new Operacion();
  operacion.num1 = 3.5;
  operacion.num2 = 2.0; 
  print('la suma es: ${operacion.sumar()}');
  operacion.restar();
  print('la multiplicacion es: ${operacion.multiplicar()}');
  
 
}
class Operacion{
  double? num1;
  double? num2;
  
  double sumar(){
    double s = num1! + num2!; 
    return s;
  }
  
  void restar(){
    double r = num1! - num2!; 
    print('la resta es: $r');    
  }
  
  double multiplicar(){
    double m = num1! * num2!; 
    return m;
  }
  
}

```

## 30 de octubre 2022

### Dart TIPOS DE PARAMETROS Y CONTRUCTORES 

```
void main(){
  
  Person person = new Person (n: 'andrea ', s: 'femenino');
  
  person.apellido = 'guitierrez';
  person.edad = 19;
  print('El nombre completo es: ${person.nombreCompleto()}');
  person.edadMas(20);
  
}
class Person{
  String? nombre, apellido, sexo;
  int? edad;
  Person({String? n, String? s}){
    nombre = n; 
    sexo = s; 
   }
  String nombreCompleto(){
    String nc = nombre! + apellido!;
    return nc;
   }
  void edadMas(int? edm){
    int num = edad! + edm!;
    print('La edad sumada es: $num');
  }
}

```
## 03 de octubre 2022

### Dart Herencia
```
void main(){
  
  Conejo conejo = new Conejo();
  
  conejo.nombre = 'conejo';
  conejo.edadPromedio = 9;
  conejo.tiporepro = 'sexual';
  conejo.alimento = 'zanahoria, lechuga';
  
  Leon leon = new Leon();
  
  leon.nombre = 'leon';
  leon.edadPromedio = 15;
  leon.tiporepro = 'sexual';
  leon.alimento = 'antilopes, bufalos';
  
  Hiena hiena = new Hiena(); 
  
  hiena.nombre = 'hiena';
  hiena.edadPromedio = 25;
  hiena.tiporepro = 'sexual';
  hiena.alimento = 'serpientes, lagartos';
  
  Hombre hombre = new Hombre();
  
  hombre.nombre = 'hombre';
  hombre.edadPromedio = 72;
  hombre.tiporepro = 'sexual';
  hombre.alimento = 'carnes, vegetales, frutas, cereales';
  
  print("""
  animal 1
  El nombre es: ${conejo.nombre}.
  La edad promedio es: ${conejo.edadPromedio} anos. 
  Su tipo de reproduccion es: ${conejo.tiporepro}.
  Se alimenta de: ${conejo.alimento}.
  
  animal 2 
  El nombre es: ${leon.nombre}.
  La edad promedio es: ${leon.edadPromedio} anos. 
  Su tipo de reproduccion es: ${leon.tiporepro}.
  Se alimenta de: ${leon.alimento}.
  
  animal 3
  El nombre es: ${hiena.nombre}.
  La edad promedio es: ${hiena.edadPromedio} anos. 
  Su tipo de reproduccion es: ${hiena.tiporepro}.
  Se alimenta de: ${hiena.alimento}.
  
  animal 4
  El nombre es: ${hombre.nombre}.
  La edad promedio es: ${hombre.edadPromedio} anos. 
  Su tipo de reproduccion es: ${hombre.tiporepro}.
  Se alimenta de: ${hombre.alimento}.
  """);

}
class Animal{
  String? nombre;
  int? edadPromedio;
  String? tiporepro;
  String? alimento;
  
}
class Hervivoro extends Animal{
  String tipo = 'Hervivoro';
}
class Conejo extends Hervivoro{}
class Carnivoro extends Animal{
  String tipo = 'Carnivoro';
}
class Leon extends Carnivoro{}
class Hiena extends Carnivoro{}
class Omnivoro extends Animal{
  String? tipo = 'Omnivoro';
}
class Hombre extends Omnivoro{}
```

## 05 de octubre 2022

### MANEJO DE CADENAS DART
```
void main(){
 
 Empresa empresa1 = new Empresa(numero: 2545, oficina: 'Nestlé', pais: 'Panama');
 Empresa empresa2 = new Empresa(oficina: 'Luxottica', pais: 'Italia', numero: 1245);
 Empresa empresa3 = new Empresa(pais: 'Espana', numero: 2365, oficina: 'INDITEX');
  
 print("""
 Empresa 1:
 
 Pais: ${empresa1.pais}
 Numero: ${empresa1.numero}
 Oficina: ${empresa1.oficina}
 Codigo: ${empresa1.generarCodigo()}
 """);
 empresa1.cantCaracteres();
  
 print("""
 Empresa 2: 
 
 Pais: ${empresa2.pais}
 Numero: ${empresa2.numero}
 Oficina: ${empresa2.oficina}
 Codigo: ${empresa2.generarCodigo()}
 """);
 empresa2.cantCaracteres();
 
 print("""
 Empresa 3:
 
 Pais: ${empresa3.pais}
 Numero: ${empresa3.numero}
 Oficina: ${empresa3.oficina}
 """);
 empresa3.cantCaracteres();
}
class Empresa{
  String? pais, oficina;
  int? numero;
  
  Empresa({this.numero, this.oficina, this.pais});
String generarCodigo(){
 String? cod = pais!.substring(0,3) + numero!.toString().substring(0,2) + oficina!.substring(oficina!.length - 3);
 return cod;
}
void cantCaracteres(){
  int cantP = pais!.length;
  int cantN = numero!.toString().length;
  int cantO = oficina!.length;
 print("""
 Cantidad de caracteres: 
 Pais: $cantP
 Numero: $cantN
 Oficina: $cantO
""");
}
}
```
## 07 de octubre 2022

### CLASE ABSTRACTA Y METODOS ESTATICOS DART
```
void main() {
  Vaca vaca = Vaca(); 
  vaca.emitirSonido();
  
  Gato gato = Gato();
  gato.emitirSonido(); 
  
  Perro perro = Perro();
  perro.emitirSonido();
  perro.nombre = 'El nombre es: bult';
  print(perro.nombre);
  Carnivoro.imc(25,15);
}
abstract class Animal{
  void emitirSonido();
}
class Vaca implements Animal{
  @override
  void emitirSonido(){
    print('El sonido de la vaca es: muu'); 
  }
}
class Gato implements Animal{
  @override
  void emitirSonido(){
    print ('El sonido de el gato es: miau');
  }
}
class Carnivoro{
  String? nombre;
  
  static void imc(int altura, int peso){
    int? calculo = altura * peso;
    print('La imc es: $calculo');
  }
}
class Perro extends Carnivoro implements Animal{
  @override
  void emitirSonido(){
    print ('El sonido de el perro es: guau');
  }
}
```

## 09 de noviembre 2022

### Desarrollo Con peticion GET a Backend un Objeto Flutter 

## main

~~~
import 'package:flutter/material.dart';
import 'widgets/Template.dart';
import 'widgets/user.dart';
import 'package:http/http.dart' as http;

void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'my app',
      home: Scaffold(
        appBar: AppBar(
        title: Text('Usuario'),
      ),
      body: FutureBuilder<User>(
        future: getUser(),
        builder: (context, snapshot) {
        if (snapshot.connectionState == ConnectionState.done) {
             User user = snapshot.data as User;
             return Template(user: user);
        }
        return Center(child: CircularProgressIndicator(),);
        }),
      ),
    );
  }

Future<User> getUser() async {
    final url = Uri.https('reqres.in', '/api/users/2');
    final response = await http.get(url);
    return User(response.body);
}
}
~~~

## Template

~~~
import 'package:flutter/material.dart';
import 'user.dart';

class Template extends StatelessWidget {
  const Template({Key? key, required this.user}) : super(key: key);
  final User user;

  @override
  Widget build(BuildContext context) {
    return Column(
      children: [
        SizedBox(height: 15.0,),
        Text(user.nombre!,style: TextStyle(fontSize: 25.0),),
        SizedBox(height: 15.0,),
        Image(image: NetworkImage(user.avatar!),),
        SizedBox(height: 15.0,),
        Text(user.email!,style: TextStyle(fontSize: 20.0),),
        SizedBox(height: 15.0,),
        Row(
          mainAxisAlignment: MainAxisAlignment.spaceAround,
          children: [
            Icon(
              Icons.facebook,
              color: Colors.blue,
              size: 24.0,
              semanticLabel: 'Text to announce in accessibility modes',
            ),
            Icon(
              Icons.email,
              color: Colors.red,
              size: 30.0,
            ),
            Icon(
              Icons.beach_access,
              color: Color.fromARGB(255, 131, 33, 243),
              size: 36.0,
            )
          ],
        )
      ],
    );
  }
}
~~~

## User

~~~
import 'dart:convert' as convert;

class User {
  String? nombre;
  String? avatar;
  String? email;

  User(String json) {
    final jsonResponse = convert.jsonDecode(json);
    nombre = jsonResponse["data"]["first_name"];
    avatar = jsonResponse["data"]["avatar"];
    email = jsonResponse["data"]["email"];
  }
}
~~~

## 16 de noviembre 2022

## Desarrollo Con peticion GET a Backend Lista Objetos

## main

~~~
import 'package:flutter/material.dart';
import 'package:http/http.dart' as http;
import 'widgets/ItemData.dart';
import 'widgets/user.dart';

void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
        title: 'MyApp',
        home: Scaffold(
          appBar: AppBar(
              title: Text('Usuarios', style: TextStyle(color: Colors.black)),
              backgroundColor: Colors.white),
          backgroundColor: Colors.black,
          body: FutureBuilder<List<User>>(
            future: getData(),
            builder: (context, snapshot) {
              if (snapshot.connectionState == ConnectionState.done) {
                List<User> users = snapshot.data!;
                return ListView.builder(
                    itemCount: users.length,
                    itemBuilder: (BuildContext context, index) {
                      final user = users[index];
                      return ItemData(user: user);
                    });
              }
              return Center(child: CircularProgressIndicator());
            },
          ),
        ));
  }

  Future<List<User>> getData() async {
    final url = Uri.https('reqres.in', '/api/users');
    final response = await http.get(url);
    return userFromJson(response.body);
  }
}
~~~

## ItemData

~~~
import 'package:flutter/material.dart';
import 'package:flutter_application_1/widgets/user.dart';

class ItemData extends StatelessWidget {
  const ItemData({
    Key? key,
    required this.user,
  }) : super(key: key);

  final User user;

  @override
  Widget build(BuildContext context) {
    return Column(
      children: [
        ListTile(
          title: Text('${user.firstName!} ${user.lastName!}',
              style: TextStyle(color: Colors.white)),
          subtitle: Text(user.correoElectrnico!,
              style: TextStyle(color: Colors.white)),
          leading: CircleAvatar(
            backgroundImage: NetworkImage(user.avatar!),
          ),
          trailing: const Icon(
            Icons.arrow_forward_ios,
            color: Colors.blue,
          ),
        ),
        Divider(),
      ],
    );
  }
}
~~~

## User

~~~
import 'dart:convert';

List<User> userFromJson(String str) =>
    List<User>.from(json.decode(str)['data'].map((x) => User.fromJson(x)));

class User {
  User({
    this.correoElectrnico,
    this.firstName,
    this.lastName,
    this.avatar,
  });
  String? correoElectrnico;
  String? firstName;
  String? lastName;
  String? avatar;

  factory User.fromJson(Map<String, dynamic> json) => User(
        correoElectrnico: json["email"],
        firstName: json["first_name"],
        lastName: json["last_name"],
        avatar: json["avatar"],
      );
}
~~~

## 23 de noviembre 2022

## CustomPaint, Stack y positioned

## main

~~~
import 'package:flutter/material.dart';
import 'package:http/http.dart' as http;
import 'widgets/background1.dart';
import 'widgets/user.dart';

void main() {
  runApp(Miapp());
}

class Miapp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      title: 'usuario',
      home: Scaffold(
        body: FutureBuilder<User>(
          future: getUser(),
          builder: (context, snapshot) {
            if (snapshot.connectionState == ConnectionState.done) {
              User user = snapshot.data as User;
              return Stack(children: [
                Background1(),
                Positioned(
                  top: 70.0,
                  left: 60.0,
                  right: 60.0,
                  child: Container(
                    width: 130.0,
                    height: 100.0,
                    child: Image(
                      image: NetworkImage(user.avatar!),
                      height: 300.0,
                    ),
                  ),
                ),
                Positioned(
                  bottom: 50.0,
                  left: 60.0,
                  right: 60.0,
                  child: Container(
                    width: 190.0,
                    height: 150.0,
                    child: Column(
                      children: [
                        SizedBox(
                          height: 5.0,
                        ),
                        Text(
                          user.nombre!,
                          style: TextStyle(
                              fontSize: 25.0, fontWeight: FontWeight.bold),
                        ),
                        SizedBox(height: 5.0),
                        Text(user.email!),
                        SizedBox(
                          height: 5.0,
                        ),
                        Row(
                          mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                          children: [
                            Icon(
                              Icons.mail,
                              color: Colors.pink,
                              size: 24.0,
                              semanticLabel:
                                  'text to announce in accessibility modes',
                            ),
                            Icon(
                              Icons.add_ic_call_rounded,
                              color: Colors.pink,
                              size: 30.0,
                            ),
                            Icon(
                              Icons.facebook,
                              color: Colors.pink,
                              size: 36.0,
                            ),
                          ],
                        ),
                      ],
                    ),
                  ),
                ),
              ]);
            }
            return Center(child: CircularProgressIndicator());
          },
        ),
      ),
    );
  }

  Future<User> getUser() async {
    final url = Uri.https('reqres.in', '/api/users/8');
    final response = await http.get(url);
    return User(response.body);
  }
}
~~~

## background1

~~~
import 'package:flutter/material.dart';

class Background1 extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Container(
      height: double.infinity,
      width: double.infinity,
      child: CustomPaint(
        painter: _HeaderLoginPainter(),
      ),
    );
  }
}

class _HeaderLoginPainter extends CustomPainter {
  @override
  void paint(Canvas canvas, Size size) {
    Paint paint = Paint();
    paint.color = Colors.pink;
    var path = Path();
    path.lineTo(0, size.height - size.height / 1.5);
    path.lineTo(size.width / 1.2, size.height / 1.8);
    path.lineTo(size.width, size.height - size.height / 1.5);
    path.lineTo(size.width, 0);
    path.close();
    canvas.drawPath(path, paint);
  }

  @override
  bool shouldRepaint(covariant CustomPainter oldDelegate) {
    return true;
  }
}
~~~

## user

~~~
import 'dart:convert' as convert;
import 'template.dart';

class User {
  String? nombre;
  String? apellido;
  String? avatar;
  String? email;

  User(String json) {
    final jsonResponse = convert.jsonDecode(json);
    nombre = jsonResponse['data']['first_name'];
    apellido = jsonResponse['data']['last_name'];
    avatar = jsonResponse['data']['avatar'];
    email = jsonResponse['data']['email'];
  }
}
~~~

## 25 de noviembre 2022

## Html Básico

## index

```
<!DOCTYPE html>
<html lang="es-CO">
    <head>
        <meta charset="UTF-8">
        <title>Sitio web</title>
    </head>
    <body>
        <h1>Paginas</h1>
        <br>
        <a href="mision.html">ir a mision</a>
        <br>
        <a href="vision.html">ir a vision</a>
        <br>
        <a href="valores.html">ir a valores</a>
        <br>
        <a href="objetivos.html">ir a objetivos</a>
    </body>
</html>

```
## mision

```
<!DOCTYPE html>
<html lang="es-CO">
<head>
    <meta charset="UTF-8">
    <title>mision</title>
</head>
<body>
    <h2>mision</h2>
    <br>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Maiores quidem veniam autem sed eveniet, iusto quibusdam dolorem obcaecati error exercitationem minima cumque reiciendis quas, aliquid dignissimos, qui itaque incidunt molestias.</p>
    <br>
    <a href="index.html">ir a inicio</a>
</body>
</html>
```
## vision
```
<!DOCTYPE html>
<html lang="es-CO">
<head>
    <meta charset="UTF-8">
    <title>vision</title>
</head>
<body>
    <h2>vision</h2>
    <br>
    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Et, dolores commodi. Voluptatibus soluta vero voluptatem numquam. Eum rem ex corporis. Delectus nulla enim dolorem labore accusamus aliquam tempore placeat voluptate.</p>
    <a href="index.html">ir a inicio</a>
</body>
</html>
```

## valores
```
<!DOCTYPE html>
<html lang="es-CO">
<head>
    <meta charset="UTF-8">
    <title>valores</title>
</head>
<body>
    <h2>valores</h2>
    <br>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Alias repellendus autem optio exercitationem accusamus at, provident maiores expedita reprehenderit nulla iure qui dolorum? Architecto beatae repudiandae sed, quasi ratione nesciunt.</p>
    <br>
    <a href="index.html">ir a inicio</a>
</body>
</html>
```
## objetivos 

```
<!DOCTYPE html>
<html lang="es-CO">
<head>
    <meta charset="UTF-8">
    <title>objetivos</title>
</head>
<body>
    <h2>objetivos</h2>
    <br>
    <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Dolorum atque fugit explicabo hic, vel vero consectetur iure magni nulla. Provident dicta reiciendis officiis distinctio, eius voluptatum iure doloremque cupiditate neque.</p>
    <br>
    <a href="index.html">ir a inicio</a>
</body>
</html>
```

## 28 de noviembre 2022

## Maquetado Html Veterinaria

## index

~~~
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <link rel="stylesheet" href="estilos.css">
    <title>Caninos</title>
</head>
<body>
    <main>
        <header><img src="img.png" alt="imagen"></header>
        <nav>
            <ul>
                <li>.Servicios.</li>
                <li>.Productos.</li>
                <li>.Guardías.</li>
                <li>.Promociones.</li>
            </ul>
        </nav>
        <section>
            <article class= "arriba">
                <h3>Cuidados y educacion para su perro</h3>
                <br>
                <p><img class="derecha" src="perro1.png" alt="perro1">Cuando decide tener un perro no sabe, no vienen con un manual de instrucciones. El perro NO es un juguete ni se debe regalar a alguien que no esté preparado.</p>
                <br>
                <a href="https://www.clinicaveterinarialaasuncion.com/blog/educacion-y-cuidados-basicos-en-perros-y-gatos/">ver mas...</a>
            </article>
            <article class= "abajo">
                <h3>Salir de viaje con su mascota</h3>
                <br>
                <p><img clase="derecha" src="perro2.png" alt="perro2">Sin importar si son perros o gatos, la raza, el tamaño o el lugar de la aeronave en el que viajan, estas mascotas, corren peligro de sufrir cualquier episodio.</p>
                <br>
                <a href="https://www.elcolombiano.com/cultura/mascotas/consejos-de-medicos-veterinarios-para-viajar-en-avion-con-perros-o-gatos-NE16470490">  ver mas...</a>
            </article>
        </section>
        <aside>
            <header>
                <h4>Solicitar cita medica</h4>
            </header>
            <form>
                <ul>
                    <li><label>Mascota: </label>
                        <input type="text" placeholder="ingrese nombre"><br><br></li>
                    <li><label>Edad: </label>
                        <input type="text" placeholder=""><br><br></li>
                    <li><label>Raza: </label>
                        <input type="text" placeholder="ingrese raza"><br><br></li>
                    <li><label>Fecha: <input type="dd/mm/aaaa"></label><br><br></li>
                    <li><label>Hora: <input type="--:-- ----"></label><br><br></li>
                    <li><label>Amo: <input type="ingrese nombre"></label><br><br></li>
                </ul>
                <button class="bnt success">validar cita</button>
            </form>
        </aside>
        <footer>
            <p>
               Contactenos 
               <br>
               Linea gratuita 018000-00001
               <br>
               Correo: preguntas@caninosyfelinos.com
            </p>
        </footer>
    </main>
</body>
</html>
~~~

## estilos

~~~
*{
    margin: 0;
    padding: 0;
}
main{
    height: 680px;
    margin: auto;
    width: 700px;
}
header{
    height: 150px;
}
header img{
    height: 150px;
    width: 698px;
}
nav{
    background-color: #1c4a48;
    height: 45px;
    border-radius: 0px 0px 15px 15px;
    padding-top: 25px;
}
ul li {
    display: inline;
    color: white;
    font-size: 19px;
    border-right: 2px solid white;
    padding: 8px 30px;
    text-align: center;
}
section{
    height: 370px;
    float: left;
    width: 375px;
    margin: 10px 0px 10px 0px;
}
.arriba{
    height: 180px;
    background-color: #fbf5b9;
    border-radius: 15px;
    border-radius: 15px 15px 0px 0px;
}
section img{
    border: 2px solid black;
    height: 120px;
    width: 120px;
    border-radius: 10px;
    float: right;
    margin-right: 10px;
}
.abajo{
    height: 180px;
    background-color: #fbf3b9;
    border-radius: 0px 0px 15px 15px;
    margin-top: 7px;
}
aside{
    height: 370px;
    display: inline-block;
    width: 310px;
    border-radius: 15px;
    background-color: #4a6e6e;
    margin: 10px 0px 8px 11px;
}
aside header{
    height: 15px;
    background-color:#0a2826;
    border-radius: 15px 15px 0px 0px;
    color: white;
    text-align: center;  
    padding: 10px 10px;
    font-size: 17px;
}
aside ul li{
    font-size: 18px;
    display: block;
    text-align: left;
    padding: 4px 25px;
}
aside input{
    height: 15px;
    width: 180px;
}
.bnt{
    border: 1px solid black;
    border-radius: 3px;
    display: block;
    margin-right: auto;
    margin-left: auto;
    height: 25px;
    width: 110px;
}
footer{
    height: 70px;
    background-color: #0a2826;
    color: #94a4a6;
    text-align: center;
    border-radius: 0px 0px 15px 15px;
}
~~~

## 02 de diciembre 2022

## Maquetado Html Banco
## index

~~~
<!DOCTYPE html>
<html lang="es-CO">
<head>
    <meta charset="UTF-8">
    <link rel="stylesheet" href="estilos.css">
    <title>Banco</title>
</head>
<body>
    <main>
        <header>
            <img src="header.png" alt="error">
        </header>
        <nav>
            <ul>
                <li>.Creditos.</li>
                <li>.leasing.</li>
                <li>.Ahorros.</li>
                <li>Servicio al cliente.</li>
            </ul>
        </nav>
        <section>
            <article class="arriba">
                <header class="titulo" id="dosb">INGRESA A TU CUENTA</header>
                <form>
                <ul>
                    <li><label>Cuenta: </label>
                        <input type="number" placeholder=" Numero de cuenta"><br><br>
                    </li>
                    <li><label>Tipo: </label>
                        <input type="text"><br><br>
                    </li>
                    <li><label>Clave: </label>
                        <input type="text" placeholder=" Ingrese Nombre"><br><br>
                    </li>
                </ul>
                <button>Ingresar</button>
                </form>
            </article>
            <article class="abajo">
                <ul>
                    <li class="df">TRANSACCIONES</li>
                    <li class="ig">Banca personal</li>
                    <li class="ig">Banca empresarial</li>
                    <li class="ig">Banca seguros</li>
                    <li class="ig">Pago de facturas</li>
                    <li class="df">TARJETAS DE CREDITO</li>
                    <li class="ig">Credi Visa</li>
                    <li class="ig">Credi Mastercard</li>
                </ul>
            </article>
        </section>
        <aside>
            <article id="topizquierda">
                <header class="titulo"  id="topizquierda">SOLICITA NUESTROS PRODUCTOS</header>
                <img src="snp.png" alt="error">
                <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Veniam maxime</p>
            </article>
            <article id="topderecha">
                <header class="titulo"  id="topderecha">AHORRRO ESTUDIANTIL</header>
                <img src="ae.png" alt="error">
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequat</p>
            </article>
            <article id="bizquierdo">
                <header class="titulo">CREDITOS VIHICULOS</header>
                <img src="cv.png" alt="error">
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Rerum mollitia </p>
            </article>
            <article id="bderecho">
                <header class="titulo">CREDITOS HIPOTECARIO</header>
                <img src="ch.png" alt="error">
                <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nemo laborum sequ</p>
            </article>
        </aside>
        <footer>
            <p>
                contactenos
                <br>
                linea gratuita 018000-00001
                <br>
                Banco entidad financiera - Todos los derechos reservados.
            </p>
        </footer>
    </main>
</body>
</html>
~~~

## estilos

~~~
*{
    margin: 0;
    padding: 0;
}
main{
    height: 840px;
    margin: auto;
    width: 850px;
}
header{
    height: 173px;
}
header img{
    border-radius: 15px 15px 0px 0px;
    width: 849px;
}
nav{
    background-color: #f6bd18;
    border-radius: 0px 0px 10px 10px;
    height: 65px;
    padding-bottom: 10px;
}
nav ul{
    padding-top: 25px;
}
ul li{
    border-right: 2px solid white;
    color: black;
    display: inline;
    font-size: 20px;
    padding: 8px 50px;
}
section{
    float: left;
    height: 490px;
    padding-top: 10px;
    width: 283px;
}
.arriba{
    background-color: #b2b2b2;
    border-radius: 15px 15px 0px 0px;
    height: 190px;
    margin-bottom: 10px;
    width: 272px;
}
.arriba ul li{
    border-right: 0px;
    font-size: 18px;
    padding: 10px 20px;    
}
.arriba input{
    height: 15px;
    width: 150px;
}
.arriba button{
    background-color: #f6bd18;
    border: 2px solid black;
    border-radius: 5px;
    color: black;
    display: block;
    margin-right: auto;
    margin-left: auto;
    width: 90px;
}
.titulo{
    background-color: #232323;
    border: 1px solid black;
    color: #a3a3a3;
    height: 40px;
    text-align: center;
    width: 270px;
}
#dosb{
    border-radius: 15px 15px 0px 0px;
}
.abajo{
    background-color: #232323;
    height: 275px;
    width: 275px;
}
.abajo ul li{
    display: block;
    font-size: 15px;
    text-align: center;
}
.ig{
    color: #a3a3a3;
    margin-bottom: 1px solid #a3a3a3;
    border-bottom: 1px solid #343434;
}
.df{
    background-color: black;
    color: #f6bd18;
}
aside{
    float: right;
    height: 475px;
    width: 560px;
    padding-top: 10px;
}
article{
    background-color: #c7c7c7;
    height: 233px;
    width: 270px;
    display: inline-block;
}
#topizquierda{
    margin-bottom: 10px;
    border-radius: 15px 0px 0px 0px;
}
#topderecha{
    margin-bottom: 10px;
    border-radius: 0px 15px 0px 0px;
    float: right;
}
#bizquierdo{
    border-radius: 0px 0px 0px 15px;
}
#bderecho{
    border-radius: 0px 0px 15px 0px;
    float: right;
}
aside img{
    height: 110px;
    width: 240px;
    border-radius: 10px;
}
aside article{
    text-align: center;
}
footer{
    background-color: #232323;
    border-radius: 0px 0px 15px 15px;
    height: 70px;
    color:#a3a3a3;
    clear: both;
    text-align: center;
    padding-top: 10px;
}
~~~