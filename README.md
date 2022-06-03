# GTEC_linux_week14

2022.06.03.Fri

nano read.sh    
#!/bin/sh    
echo "데이터를 입력해주세요"

read var1    
echo $var1

nano newif.sh    
#!/bin/sh    
if [ 5 -eq 1 ]    
then    
  echo "참입니다."    
else    
  echo "거짓입니다."    
fi

expr [수식1] + [수식2] -> 띄어쓰기 해야지 실행됨    
expr 5 + 3    
expr 5 - 3    
expr 5 \* 3 -> * 가 모두를 지칭하는 특수문자이기도 하기 때문에 \*로 작성해야함

#!/bin/sh    
num=100 + 200 -> 300으로 저장되지 않음    
echo $num

nano num.sh    
#!/bin/sh    
num=`expr 100 + 200` -> num = `expr 100 + 200`으로 쓰면 에러남 변수 선언 시 띄어쓰지 말 것    
echo $num

nano num1.sh    
#!/bin/sh    
num=`expr \( 200 + 300 \) \* 2` -> 괄호도 char 형태로 인식되지 않기 위해 앞에 \를 붙여주고 괄호 안에서 계산을 하기 위해서 앞뒤로 공백을 줘야함    
echo $num

nano case.sh    
#!/bin/sh    
echo "리눅스 수업이 재미있나요? (Y or N)"    
read var1

case $var1 in    
  [yY]*) -> y와 Y로 시작하는 모든 단어    
    echo "너가 진리야 짱";;    
   [nN]*)    
    echo "섭섭해";;    
   *)    
    echo "잘 입력해야지";;    
esac

nano for.sh    
#!/bin/sh    
num=0

for i in 1 2 3    
  do    
    num=`expr $num + $i`    
    echo "num값: "$num    
    echo "i값: "$i    
  done

while [ 조건 ]    
  do    
    반복문    
   done
