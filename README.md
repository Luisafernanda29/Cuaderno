# Cuaderno
Aqui podremos ver mis notas 

```

# sub cuaderno
  msgbox "hola sena" 
  msgbox "hola mundo"
# and sub

```

## 26 de agosto 20222

### PROGRAMA:

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

### PROGRAMA:

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

### PROGRAMA:

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

### PROGRAMA:

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


### PROGRAMA:

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


### PROGRAMA:

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

### PROGRAMA:

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

### PROGRAMA

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

### PROGRAMA DART

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

### PROGRAMA DART2 

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