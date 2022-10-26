# Cuaderno
Aqui podremos ver mis notas 

## PRIMER PROGRAMA
```

# sub cuaderno
  msgbox "hola sena" 
  msgbox "hola mundo"
# and sub

```

## 26 de agosto 20222

### PROGRAMA CONDICIONAL SI 

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

### PROGRAMA CASO

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

### PROGRAMA FOR 

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

## 31 de agosto 2022

### PROGRAMA FOR 2

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


### PROGRAMA FOR 3

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


### PROGRAMA FOR 4

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

## 09 de septiembre 2022

### PROGRAMA CICLO MQ 1

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

## 09 de septiembre 2022

### PROGRAMA CICLO MQ 2

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

## 28 de septiembre 2022

### PROGRAMA DART, OBJETOS, CLASES Y METODOS

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

## 03 de octubre 2022

### PROGRAMA TIPOS DE PARAMETROS Y CONTRUCTORES DART

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

## 10 de octubre 2022

### PROGRAMA MANEJO DE CADENAS DART
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

## 10 de octubre 2022

### PROGRAMA HERENCIA DART
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

## 21 de octubre 2022

### PROGRAMA CLASE ABSTRACTA Y METODOS ESTATICOS DART
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