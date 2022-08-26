# Cuaderno
Aqui podremos ver mis notas 

# sub cuaderno
 msgbox "hola sena" 
 msgbox "hola mundo"
# and sub

Sub impuesto()
    a = Int(InputBox("valor a pagar anual"))
    
    Total = a * ip
    
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
                  If a > 10000001 And a < 100000000 Then
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
