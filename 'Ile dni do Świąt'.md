```sh
#!/bin/bash

Dzien=`date +%j`
Rok=`date +%Y`

Swieta=`date +%j -d $Rok'-12-25'`

if [ $Dzien == $Swieta -o $Dzien == $Swieta+1 ];
 then
 echo " __          __              _             _        __//_         _       _    _ "
 echo " \ \        / /             | |/|         | |      / ____|       (_)     | |  | |"
 echo "  \ \  /\  / /__  ___  ___  |  /_   _  ___| |__   | (_____      ___  __ _| |_ | |"
 echo "   \ \/  \/ / _ \/ __|/ _ \/  || | | |/ __| '_ \   \___ \ \ /\ / / |/ _\ | __|| |"
 echo "    \  /\  /  __/\__ \ (_)|/| || |_| | (__| | | |  ____) \ V  V /| | (_| | |_ |_|"
 echo "     \/  \/ \___||___/\___/ |_| \__, |\___|_| |_| |_____/ \_/\_/ |_|\__, |\__|(_)"
 echo "                                 __/ |                                  \\       "
 echo "                                |___/                                            ";

else

 Ile=`expr $Swieta - $Dzien`

 if [ $Ile -gt 0 ];
  then
  echo "Do Swiat Bozego Narodzenia zostalo $Ile dni";

 else

  Rok2=`expr $Rok + 1`
  Swieta2=`date +%j -d $Rok2'-12-24'`

  Koniec=`date +%j -d $Rok'-12-31'`
  Pom=`expr $Koniec - $Dzien`

  Ile2=`expr $Swieta2 + $Pom`
  echo "Do Swiat Bozego Narodzenia zostalo $Ile2 dni";

 fi

  echo "         *"
  echo "        (')&"
  echo "      & / \|"
  echo "      |/   \ "
  echo "      '-   -'"
  echo "       / & \ &"
  echo "    & /  |  \|"
  echo "    |/_     _\ "
  echo "      /     \ &"
  echo "   & /    &  \|"
  echo "   |/     |   \ "
  echo "   '-----,-----'";

fi

exit 0
```
