unit Unit1;

interface

uses
  Winapi.Windows, Winapi.Messages, System.SysUtils, System.Variants, System.Classes, Vcl.Graphics,
  Vcl.Controls, Vcl.Forms, Vcl.Dialogs, Vcl.StdCtrls;

type
  TForm1 = class(TForm)
    Button1: TButton;
    ta: TEdit;
    tb: TEdit;
    tc: TEdit;
    Memo1: TMemo;
    procedure Button1Click(Sender: TObject);
    procedure taClick(Sender: TObject);
    procedure tbClick(Sender: TObject);
    procedure tcCliak(Sender: TObject);

  private
    { Private declarations }
  public
    { Public declarations }
  end;

var
  Form1: TForm1;

implementation
var
  a:integer;
  b:integer;
  c:integer;
  x1:double;
  x2:double;
  d:double;


{$R *.dfm}

procedure TForm1.taClick(Sender: TObject);
begin
    ta.clear;
end;

procedure TForm1.tbClick(Sender: TObject);
begin
tb.clear;
end;

procedure TForm1.tcCliak(Sender: TObject);
begin
tc.clear;
end;

procedure TForm1.Button1Click(Sender: TObject);
begin
  if (ta.text = '')    then
    begin
       ShowMessage('Введите a');
       exit;
    end;
     if (tb.text = '')    then
    begin
       ShowMessage('Введите b');
       exit;
    end;
     if (tc.text = '')    then
    begin
       ShowMessage('Введите c');
       exit;
    end;

  if TryStrToInt(ta.text, a)
      and TryStrToInt(tb.text, b)
      and TryStrToInt (tc.text, c)
      then
        begin
          if a=0 then
          begin
            ShowMessage('a не может быть 0');
            exit;
          end;
          d:=(b*b)-(4*a*c);
            if (d<0) then
            begin
            ShowMessage('Действительных корней нет дискрименант меньше 0');
            exit;
            end;
            if (d=0) then
              begin
                x1:=(b*(-1))/2*a;
                memo1.lines.text:=('x1 = ')+FloatToStr(x1);
                exit;
              end;
            x1 := (((-1 * b) + sqrt(d)) / (2*a));
            x2 := (((-1 * b) - sqrt(d)) / (2*a));
            memo1.lines.text:=('x1 = ')+FloatToStr(x1);
            memo1.Lines.Add(('x2 = ')+FloatToStr(x2));
        end
  else ShowMessage('Неверные значения!');
end;


end.
