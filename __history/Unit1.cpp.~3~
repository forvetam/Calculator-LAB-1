//---------------------------------------------------------------------------

#include <vcl.h>
#pragma hdrstop

#include "Unit1.h"
//---------------------------------------------------------------------------
#pragma package(smart_init)
#pragma resource "*.dfm"
TForm1 *Form1;
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
        TButton * button = dynamic_cast<TButton*>(Sender);
		Edit1->Text+= button->Caption;
	}


}
//---------------------------------------------------------------------------

