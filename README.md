# Cuaderno
Aqui podremos ver mis notas 

# sub cuaderno
 msgbox "hola sena" 
 msgbox "hola mundo"
# and sub

""""

26 de agosto 20222


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

"""""""

""""
26 de agosto 2022

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

""""""

29 de agosto 2022

Sub nombre()
 
 fila = 4
 
 For n = 1 To 15
    nomb = InputBox("ingrese un nombre")
    Hoja1.Cells(fila, 2) = nomb
    fila = fila + 1
 Next n
 
End Sub

"""""""