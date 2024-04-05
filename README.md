/*
 * Prelab 4.c
 *
 * Created: 4/04/2024 21:44:31
 * Author : esteb
 */ 
#define F_CPU 16000000

#include <avr/io.h>
#include <util/delay.h>

int main(void)
{
	
	DDRD |= 0xFF;
	PORTD = 0;
	UCSR0B = 0;
   
    while (1) 
    {
		switch(PINB){
			case 0:
			PORTD = PORTD;
			break;
			
			case 1:
			PORTD += 1;
			_delay_ms(500);
			break;
			
			case 2: 
			PORTD -= 1;
			_delay_ms(500);
			break;
			
			case 3:
			PORTD = PORTD;
			break;
		}
    }
}

