# Simple-Projects #pascalzin
They are just simple projects for study. 
Program calculadora; 
Var
N1, N2, SOMA, SUB, MULT: INTEGER;
OP: CHAR;
DIVI, RESULTADO: REAL;
Begin
REPEAT
  WRITELN('QUAL É O PRIMEIRO NÚMERO?');
  READLN(N1);
  WRITELN ('QUAL É O SEGUNDO NÚMERO?');
  READLN(N2);
  WRITELN('QUAL SERÁ A OPERAÇÃO ESCOLHIDA?');
  WRITELN(' 1 - SOMA ');
  WRITELN(' 2 - SUB  ');
  WRITELN(' 3 - MULTI');
  WRITELN(' 4 - DIVI ');
  WRITELN(' 5 - s.a.i.r'); 
  READLN(OP);
 CASE OP OF
      '1': BEGIN
             RESULTADO := N1 + N2;
             WRITELN('Resultado: ', RESULTADO:0:2);
           END;
      '2': BEGIN
             RESULTADO := N1 - N2;
             WRITELN('Resultado: ', RESULTADO:0:2);
           END;
      '3': BEGIN
             RESULTADO := N1 * N2;
             WRITELN('Resultado: ', RESULTADO:0:2);
           END;
      '4': BEGIN
             IF N2 = 0 THEN
               WRITELN('Erro: Divisão por zero!')
             ELSE
               BEGIN
                 RESULTADO := N1 / N2;
                 WRITELN('Resultado: ', RESULTADO:0:2);
               END;
           END;
      '5': BEGIN
             WRITELN('Saindo do programa...');
             HALT;  { O programa vai parar aqui }
           END;
    ELSE
      WRITELN('Opção inválida. Tente novamente.');
    END;

  UNTIL OP = '5';  { O laço vai continuar até o usuário escolher a opção '5' }  
End.
