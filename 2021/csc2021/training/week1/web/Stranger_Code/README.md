# Stranger Code

- Category: Web
- Points: 100


In his spare time, R-boy likes surfing the dark web looking for hidden messages. One day he finds a strange code on a website and is sure it contains a hidden message. Help him discover what the message says.

The files are added in the folder of this project.

## Resolve

To be able to resolve this you should run the code and get the output, I did by using Firefox + Debugger and stopping the executing right before the end. The variable change through the execution and thus changing the code in the _.js_ attached to :
<!-- markdownlint-disable -->
```javascript
function strrev(s){if(!s)return'';var a='';for(i=s.length-1;i>=0;i--){a+=s.charAt(i)}return a};function flag(){var a='';var b=\"7b\";b+=\"46\";b+=\"4c\";b+=\"47\";b+=\"3a\";b+=\"41\";b+=\"6c\";b+=\"6c\";b+=\"53\";b+=\"65\";b+=\"74\";b+=\"2e\";b+=\"4d\";b+=\"31\";b+=\"73\";b+=\"73\";b+=\"31\";b+=\"4f\";b+=\"6e\";b+=\"53\";b+=\"74\";b+=\"61\";b+=\"72\";b+=\"74\";b+=\"33\";b+=\"64\";b+=\"7d\";for(var i=0;i<b.length;i+=2){a+=String.fromCharCode(parseInt(b.substr(i,2),16))}return a};function magic(){var a=new Array();a[14]='x';a[3]='u';a[11]='_';a[0]='0';a[4]='5';a[15]='5';a[7]='7';a[1]='b';a[13]='u';a[8]='1';a[12]='5';a[2]='f';a[6]='4';a[10]='n';a[5]='c';a[9]='0';var b='';var c=document.getElementById(\"pw\").value;c=strrev(c);if(c==a.join(\"\")){b=\"Congratulation! The flag is: \"+flag()}else{b=\"Try again :(\"}document.getElementById(\"result\").innerHTML=b};"
```
<!-- markdownlint-restore -->
I initially thought the password was necessary to complete this challenge and so I started working on a[] array which is in clear text but then realized that changing the **b** variable parts using ASCII hex codification give the **FLAG**:

```verbatim
{FLG:AllSet.M1ss1OnStart3d}
```
