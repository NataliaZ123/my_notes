#delphi [[Delphi]]
try
   some code
  //сама делфи выбрасывает исключение или if .. then raise Exception.Create('Свой текст');
  //some code - не выполняется в случае исключения
except//выполняется если exception
  {on e: Exception do
    begin
      WriteLn(ErrOutput, e.Message);
      ExitCode := 1;
    end;}
  //или другой свой код
end;

или сложнее

...
 try
    ...
    try
      ...//some code
    except//if delphi throws exception
      ...
      Exit;//exits out(or to finally if finally)
    end;
    ... 
 finally
    f.Free;//some object
 end;
...