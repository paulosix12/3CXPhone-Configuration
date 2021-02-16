Script para configuração do 3cxPhone


@echo off
TASKKILL /F /IM 3CXPhone.exe /T
cls
set /p fullname=Digite seu nome:
set /p extension=Digite seu Ramal:
cls
REM mkdir "c:%HOMEPATH%\locals~1\applic~1\3CX VoIP Phone"
echo [Profile0] > "%LOCALAPPDATA%\3CX VoIP Phone\3CXVoipPhone.ini"
echo Name=%fullname% >> "%LOCALAPPDATA%\3CX VoIP Phone\3CXVoipPhone.ini"
echo AuthUser=%extension% >> "%LOCALAPPDATA%\3CX VoIP Phone\3CXVoipPhone.ini"
echo AuthID=%extension% >> "%LOCALAPPDATA%\3CX VoIP Phone\3CXVoipPhone.ini"
echo AuthPass=%extension% >> "%LOCALAPPDATA%\3CX VoIP Phone\3CXVoipPhone.ini"
echo CallerID=%fullname% >> "%LOCALAPPDATA%\3CX VoIP Phone\3CXVoipPhone.ini"
echo PBXVoicemail= >> "%LOCALAPPDATA%\3CX VoIP Phone\3CXVoipPhone.ini"
echo Enabled=1 >> "%LOCALAPPDATA%\3CX VoIP Phone\3CXVoipPhone.ini"
echo PBXAddr=COLOQUE O IP AQUI >> "%LOCALAPPDATA%\3CX VoIP Phone\3CXVoipPhone.ini"
echo PBXRemoteAddr= >> "%LOCALAPPDATA%\3CX VoIP Phone\3CXVoipPhone.ini"
echo ServerProxy= >> "%LOCALAPPDATA%\3CX VoIP Phone\3CXVoipPhone.ini"
echo DtmfRFC2833=1 >> "%LOCALAPPDATA%\3CX VoIP Phone\3CXVoipPhone.ini"
echo DtmfInband=0 >> "%LOCALAPPDATA%\3CX VoIP Phone\3CXVoipPhone.ini"
echo DtmfSipinfo=0 >> "%LOCALAPPDATA%\3CX VoIP Phone\3CXVoipPhone.ini"
echo DtmfPayload=101 >> "%LOCALAPPDATA%\3CX VoIP Phone\3CXVoipPhone.ini"
echo SipTransport=0 >> "%LOCALAPPDATA%\3CX VoIP Phone\3CXVoipPhone.ini"
echo RegistrationTime=2 >> "%LOCALAPPDATA%\3CX VoIP Phone\3CXVoipPhone.ini"
echo Codecs=PCMU;PCMA;GSM; >> "%LOCALAPPDATA%\3CX VoIP Phone\3CXVoipPhone.ini"
echo VideoCodecs= >> "%LOCALAPPDATA%\3CX VoIP Phone\3CXVoipPhone.ini"
echo VideoFormats=QCIF;CIF;SQCIF;CIF4; >> "%LOCALAPPDATA%\3CX VoIP Phone\3CXVoipPhone.ini"
echo LocalPBX=1 >> "%LOCALAPPDATA%\3CX VoIP Phone\3CXVoipPhone.ini"
echo RTPTransport=0 >> "%LOCALAPPDATA%\3CX VoIP Phone\3CXVoipPhone.ini"
echo ProvisioningURL=http:// >> "%LOCALAPPDATA%\3CX VoIP Phone\3CXVoipPhone.ini"
echo UseTunnel=0 >> "%LOCALAPPDATA%\3CX VoIP Phone\3CXVoipPhone.ini"
echo UseProxy=0 >> "%LOCALAPPDATA%\3CX VoIP Phone\3CXVoipPhone.ini"
echo TunnelPass=abc >> "%LOCALAPPDATA%\3CX VoIP Phone\3CXVoipPhone.ini"
echo TunnelRemAddr= >> "%LOCALAPPDATA%\3CX VoIP Phone\3CXVoipPhone.ini"
echo TunnelPort=5090 >> "%LOCALAPPDATA%\3CX VoIP Phone\3CXVoipPhone.ini"
echo PBXPort=0 >> "%LOCALAPPDATA%\3CX VoIP Phone\3CXVoipPhone.ini"
echo STUNServer=stun.3cx.com >> "%LOCALAPPDATA%\3CX VoIP Phone\3CXVoipPhone.ini"
echo AutoProvisioning=0 >> "%LOCALAPPDATA%\3CX VoIP Phone\3CXVoipPhone.ini"
echo VoicemailConfirmed=0" >> "%LOCALAPPDATA%\3CX VoIP Phone\3CXVoipPhone.ini"


cd "C:\Program Files (x86)\3CXPhone\"

start 3CXPhone.exe
goto end
