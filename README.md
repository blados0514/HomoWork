Function Ft_Calcular_Fecha (an_Dato Number Default null) Return Date AS 
Fecha Date;
Dia Number(2);
Mes Number(2);
Año Number(4);
Dia_1 Varchar(2);
Mes_1 Varchar(2);
 
Begin
Dia:=0;
Mes:=0;
Año:=0;

Dia:=Round(Dbms_Random.Value(1,30));
    If Length(Dia)= 1 Then
        Dia_1:= '0'||dia;
    Else
        Dia_1:=Dia;
    End If;
Mes:=Round(Dbms_Random.Value(1,12));
    if Length(Mes)= 1 Then 
        Mes_1:= '0'||Mes;
    Else
        Mes_1:=Mes;
    End If;
Año:=Round(Dbms_Random.Value(1980,2017));
Fecha:=(To_Date(Dia_1||Mes_1||Año));
    Return Fecha;
END Ft_Calcular_Fecha;
