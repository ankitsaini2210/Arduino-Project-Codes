Arduino-Project-Codes
=====================
Banging LED code

//LEDs r connctd from pin 2 to 9

          void setup()
          {
             for(int i=2;i<=9;i++)
            {
              pinMode(i,OUTPUT);
            }
          }
          void loop()
          {
           int j=9;
           for(int i=2;i<=5;i++)
           {
            if(j>5)
           {
  
             digitalWrite(i,LOW);
              digitalWrite(j,LOW);
             delay(300);
             digitalWrite(i,HIGH);
             digitalWrite(j,HIGH);
           }
    
           else
          {
           j=9;
          }
          j=j-1;
         }
         int k=6;
        for(int l=5;l>=2;l--)
        {
         digitalWrite(l,LOW);
         digitalWrite(k,LOW);
         delay(300);
         digitalWrite(l,HIGH);
         digitalWrite(k,HIGH);
         k=k+1;
        }
      }

