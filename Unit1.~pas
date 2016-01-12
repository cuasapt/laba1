unit Unit1;

interface

uses
  Windows, Messages, SysUtils, Variants, Classes, Graphics, Controls, Forms,
  Dialogs, FileCtrl, StdCtrls;

type
  TForm1 = class(TForm)
    FilterComboBox1: TFilterComboBox;
    DriveComboBox1: TDriveComboBox;
    DirectoryListBox1: TDirectoryListBox;
    FileListBox1: TFileListBox;
    Button1: TButton;
    Button2: TButton;
    Button3: TButton;
    procedure Button1Click(Sender: TObject);
    procedure Button2Click(Sender: TObject);
    procedure Button3Click(Sender: TObject);
  private
    { Private declarations }
  public
    { Public declarations }
  end;

var
  Form1: TForm1;

implementation

{$R *.dfm}

procedure TForm1.Button1Click(Sender: TObject);
begin
 CreateDir('morkovka');
 ShowMessage('Новый каталог создан');
end;

procedure TForm1.Button2Click(Sender: TObject);
var
  f: TextFile;
  text :string;
begin
  AssignFile(f, 'vorobushek.txt');
  ReWrite(f);//Открыть для записи
  WriteLn(f, 'krolik');
  CloseFile(f);

  if CopyFile('vorobushek.txt','C:\Program Files\Acer\antresol.txt',true) //Скопированный файл также можно переименовать.Пример:CopyFile('Файл.txt','C:\Program Files\Borland\НОВОЕ_ИМЯ.txt',true)
    then ShowMessage('Файл скопирован')
    else ShowMessage('Файл не найден или уже существует');
end;

procedure TForm1.Button3Click(Sender: TObject);
begin
if  (DeleteFile('antresol.txt')) or (DeleteFile('vorobushek.txt'))
    then ShowMessage('Файл удален')
    else ShowMessage('Файл не найден');
  if RemoveDir('morkovka')
    then ShowMessage('ПАПКА удалена')
    else ShowMessage('Папка не найдена');
end;

end.
