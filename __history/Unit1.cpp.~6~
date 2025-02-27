//---------------------------------------------------------------------------

#include <vcl.h>
#pragma hdrstop

#include "Unit1.h"
//---------------------------------------------------------------------------
#pragma package(smart_init)
#pragma resource "*.dfm"
TForm1 *Form1;

bool has_sin = false;
//---------------------------------------------------------------------------
__fastcall TForm1::TForm1(TComponent* Owner)
	: TForm(Owner)
{
}
//---------------------------------------------------------------------------

void __fastcall TForm1::ButtonEqualClick(TObject *Sender)
{
    int i;
}
//---------------------------------------------------------------------------

void __fastcall TForm1::NumberPress(TObject *Sender)
{
	TButton * button = dynamic_cast<TButton*>(Sender);
	Edit1->Text+= button->Caption;
}
//---------------------------------------------------------------------------


void __fastcall TForm1::OperationPress(TObject *Sender)
{
	AnsiString equation = Edit1->Text;
	AnsiString LastCh = AnsiLastChar(equation);
	if (!equation.IsEmpty()) {
		if (LastCh == '+' || LastCh == '-' || LastCh == '/' || LastCh == '*') {
			equation.SetLength(equation.Length()-1);
			Edit1->Text=equation;
		}
		if (has_sin) {
			equation += ')';
            has_sin = false;
			Edit1->Text=equation;
		}
        TButton * button = dynamic_cast<TButton*>(Sender);
		Edit1->Text+= button->Caption;
	}


}
//---------------------------------------------------------------------------

void __fastcall TForm1::BackspacePress(TObject *Sender)
{
	AnsiString equation = Edit1->Text;
	equation.SetLength(equation.Length()-1);
	Edit1->Text=equation;
}
//---------------------------------------------------------------------------

void __fastcall TForm1::ClearAll(TObject *Sender)
{
	AnsiString equation = Edit1->Text;
	equation.SetLength(0);
	Edit1->Text=equation;
}
//---------------------------------------------------------------------------

void __fastcall TForm1::SinPress(TObject *Sender)
{
	AnsiString equation = Edit1->Text;
	AnsiString LastCh = AnsiLastChar(equation);
	if (equation.IsEmpty() || LastCh == '+' || LastCh == '-' || LastCh == '/' || LastCh == '*') {
		equation += 'sin';
	}
	else{
	equation += '*sin(';
	}
	Edit1->Text=equation;
}
//---------------------------------------------------------------------------

