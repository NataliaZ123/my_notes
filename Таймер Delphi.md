#delphi [[Delphi]]
Зачем таймер:
-пинговать хостинг. некоторые хостинги прерывают соединение, если его регулярно не пингуют
-нужно, чтобы приложение закрывалось после периода неактивности
-нужно обновлять данные на экране раз в период и т.д

Примерчик с таймером:

procedure TfrmTimer.FormActivate(Sender: TObject);
begin
  btnStart.Enabled := True;
  tmr1.Enabled := False;
end;

procedure TfrmTimer.btnStartClick(Sender: TObject);
begin
  btnStart.Enabled := False;
  Sec := 10;
  Randomize;
  Number := Random(10)+1;
  tmr1.Enabled := True;
end;

procedure TfrmTimer.tmr1Timer(Sender: TObject);
begin
  tmr1.Enabled := False;
  if Sec >= 1 then
  begin
    tmr1.Enabled := True;
    Sec := Sec - 1;
  end
  else
  begin
    ShowMessage('Время вышло');
    FormActivate(frmTimer);
  end;
end;