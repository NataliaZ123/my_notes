MDI(multiple-document interface) [[Delphi]] - приложения со вкладками

-При помощи TabbedNotebook;  TPageControl - одна форма, вкладки

-При помощи MainMenu и FormStyle->MDIForm/mdichild
  -MainMenu и FormStyle->MDIForm/mdichild делаем вкладочку
  -WindowState property to wsMaximized всем формам
  -Не создавать чайлд в начале(Project Options Forms и не создавать)
  -освободить всю память OnClose Action := caFree; Release; на всех чайлдах и на самой  
  -чтобы не создавало экземпляры
    try
      Form2.Show;
    except
      form2 := TForm2.Create(Self);
      Form2.Show;
    end;
    или
    if not Assigned(Form2) then
    begin
      form2 := TForm2.Create(Self);
      Form2.Show;
    end
    else Form2.Show;//Form2 := nil в юните формы при закрытии
  -чтобы просматривать разные вкладки - компонент  TdxTabbedMDIManager - поместить на главную форму и сделать Active:=True
  -чтобы у вкладок был крестик - свойство MDI Tab Manager 
  -перетаскивать вкладки - same
  -поместить на чайлд панель и для некоторых элементов на чайлде  Anchor property Top,Left,Right and Bottom чтобы правильно размещались на форме

for i := 0 To Form1.MDIChildCount - 1 Do
  begin
    if Form1.MDIChildren[i].Caption = 'Form2' Then
      MDIChildren[i].Show;
      {Здесь можно активировать дочернюю MDI-форму
    или выполнить какие-либо действия}
  end;