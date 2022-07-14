#NoEnv

Windows_Disk := A89E-DCF0

{
    RegExMatch(Windows_Disk, "(.*)windows", Disk_7)
    if Disk_71 contains Q,W,E,R,T,Y,U,I,O,P,A,S,D,F,G,H,J,K,L,Z,X,C,V,B,N,M
    {
        DriveGet, HWID, Serial, %Disk_71%
    }
       
    RegExMatch(Windows_Disk, "(.*)Windows", Disk_8)
    if Disk_81 contains Q,W,E,R,T,Y,U,I,O,P,A,S,D,F,G,H,J,K,L,Z,X,C,V,B,N,M
    {
        DriveGet, HWID, Serial, %Disk_81%
    }
       
    RegExMatch(Windows_Disk, "(.*)WINDOWS", Disk_10)
    if Disk_101 contains Q,W,E,R,T,Y,U,I,O,P,A,S,D,F,G,H,J,K,L,Z,X,C,V,B,N,M
    {
        DriveGet, HWID, Serial, %Disk_101%
    }
}
{
    MsgBox, У тебя операционная система не Windows!
    ExitApp
}

Parse := ComObjCreate("WinHttp.WinHttpRequest.5.1")
Parse.Open("GET", "https://raw.githubusercontent.com/millioner1403/index.html/master/index.html", false)
Parse.Send()
Parse.WaitForResponse()
Text := Parse.ResponseText

if Text contains %HWID%
{
    Goto, true
}
else
{
    MsgBox, Добро пожаловать в поле регистрации!`nСкопированые данные отправте автору программы.
    Gui, Font, S16 CBlack Bold, Arial
    Gui, Add, Text, x53 y0 w500 h30 , Твой ключ:
    Gui, Font, ,
    Gui, Add, Edit, x1 y31 w219 h21 +Center ReadOnly vEdit,
    Gui, Add, Button, x35 y52 w153 h24 gClip , Копировать и закрыть
    Gui, Show, w221 h76, Доступ
    GuiControl, , Edit, % HWID
    return
    Clip:
    Gui, Submit, NoHide
    Clipboard := Edit
    ExitApp
    GuiClose:
    ExitApp
}
true:
MsgBox, Добро пожаловать!
capt0:
SelectedFile := "F:\korzinaamazenka\amazing\chatlog.txt"
filedelete, %SelectedFile%
fileappend, %SelectedFile%
sleep 1
capt3:
Loop, Read, %SelectedFile%
{
IfInString, A_LoopReadLine, 1182500
{
Goto, capt5
}
}
goto, capt3
capt5:
Send, {enter down}
sleep 5
Send, {enter up}
sleep 5
Send, {down}
sleep 5
Send, {down}
sleep 3
Send, {down}
sleep 5
Send, {enter down}
sleep 5
Send, {enter up}
sleep 5
Send, {enter down}
sleep 5
Send, {enter up}
sleep 5
Send, {enter down}
sleep 5
Send, {enter up}
sleep 5
Send, {enter down}
sleep 5
Send, {enter up}
sleep 5
Send, {enter down}
sleep 5
Send, {enter up}
sleep 5
Send, {enter down}
sleep 5
Send, {enter up}
sleep 5
Send, {enter down}
sleep 5
Send, {enter up}
sleep 5
Send, {enter down}
sleep 5
Send, {enter up}
sleep 5
Send, {enter up}
sleep 5
Send, {down}
sleep 50
Send, {down}
sleep 30
Send, {down}
sleep 5
Send, {enter down}
sleep 5
Send, {enter up}
sleep 5
Send, {enter down}
sleep 5
Send, {enter up}
sleep 5
Send, {enter down}
sleep 5
Send, {enter up}
sleep 5
Send, {enter down}
sleep 5
Send, {enter up}
sleep 5
Send, {enter down}
sleep 5
Send, {enter up}
sleep 5
Send, {enter down}
sleep 5
Send, {enter up}
sleep 5
Send, {enter down}
sleep 5
Send, {enter up}
sleep 5
Send, {enter down}

goto capt0

!5::
Pause
