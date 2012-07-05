Arduino-Project-Codes
=====================
Banging LED code

//LEDs r connctd from pin 2 to 9 of arduino board

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


Security system========================================================================

//using a ir sensor nd led's cnncted to digital pins 2 to 9
     int new_val;
     int old_val=0;

     void setup()
     {
      Serial.begin(9600);
      for(int i=2;i<=9;i++)
     {
      pinMode(i,OUTPUT);
     }
    }
    
    void loop()
    {
      int new_val=analogRead(0);
      Serial.println(new_val);
      int diff=new_val-old_val;
      if(diff>150)
     {
       for(int i=2;i<=9;i++)
      {
        digitalWrite(i,LOW);
        delay(500);
        digitalWrite(i,HIGH);
      
      }
     }
     old_val=new_val;
     delay(500);
    }

