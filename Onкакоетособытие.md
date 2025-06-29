#delphi [[Delphi]]
procedure TfmDiscountBloxSets.chkShowActiveClick(Sender: TObject);
begin
  OnActivate(Self);
end;

OnActivate вызывает событие которое на этой форме висит на FormActivate
функции Onкакоетособытие при наступлении события вызываются

OnKeyDown - вызывается при нажатии любой клавиши на клавиатуре 
OnKeyUp - вызывается при отпускании любой клавиши на клавиатуре 
OnKeyPress - вызывается при нажатии клавиши, соответствующей символу ASCII
Клавиши можно распознавать и для разных(втч букв) ставить разные условия, подробнее:
https://studfile.net/preview/2428249/page:2/