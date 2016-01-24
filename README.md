Arduino_TVout_with_ps2Keyboard

This is the library that alows you to use both TVout and PS2keyboard at the same time, withought glitches
 based on pollserial.cpp and PS2Keyboard.cpp
 Combined by Yotson, october 2011
 
 ps2 keyboard library which uses the usart hardware for buffering individual bits into a byte before reading the byte by software.
 Goal was to use a ps2 keyboard in combination with tv-out without image/timing corruption. 
 The interrupt driven version of ps2 keyboard messed with tv out image/timing.
    
 Tested on atmega328. Not compatible with arduino mega/mega2560 as the XCKn pins are not broken out to header/pad.
   
 ps2-Keyboard pin   |  Arduino pin
 -------------------------------------------
 data               |  RX, digital pin 0
 clock              |  XCK, digital pin 4
 ground             |  Ground
 5V                 |  5V   

 pollserial.cpp Heavily modified version of:
 
 HardwareSerial.cpp - Hardware serial library for Wiring
 Copyright (c) 2006 Nicholas Zambetti.  All right reserved.

 Modified 23 November 2006 by David A. Mellis
 
 Modified July 2010 by Myles D. Metzler
 PS2Keyboard.cpp - PS2Keyboard library
 Copyright (c) 2007 Free Software Foundation.  All right reserved.
 Written by Christian Weichel <info@32leaves.net>
 
 ** Mostly rewritten Paul Stoffregen <paul@pjrc.com> 2010, 2011
 ** Modified for use beginning with Arduino 13 by L. Abraham Smith, <n3bah@microcompdesign.com> * 
 ** Modified for easy interrup pin assignement on method begin(datapin,irq_pin). Cuningan <cuninganreset@gmail.com> **
 
 for more information you can read the original wiki in arduino.cc
 at http://www.arduino.cc/playground/Main/PS2Keyboard
 or http://www.pjrc.com/teensy/td_libs_PS2Keyboard.html
 
 Version 2.1 (May 2011)
 - timeout to recover from misaligned input
 - compatibility with Arduino "new-extension" branch
 - TODO: send function, proposed by Scott Penrose, scooterda at me dot com
 
 Version 2.0 (June 2010)
 - Buffering added, many scan codes can be captured without data loss
 if your sketch is busy doing other work
 - Shift keys supported, completely rewritten scan code to ascii
 - Slow linear search replaced with fast indexed table lookups
 - Support for Teensy, Arduino Mega, and Sanguino added

 Slightly modified by Bill Peterson (albedozero@gmail.com) 2016
  to work with Arduino 1.6.4+
 
 This library is free software; you can redistribute it and/or
 modify it under the terms of the GNU Lesser General Public
 License as published by the Free Software Foundation; either
 version 2.1 of the License, or (at your option) any later version.
 
 This library is distributed in the hope that it will be useful,
 but WITHOUT ANY WARRANTY; without even the implied warranty of
 MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU
 Lesser General Public License for more details.
 
 You should have received a copy of the GNU Lesser General Public
 License along with this library; if not, write to the Free Software
 Foundation, Inc., 51 Franklin St, Fifth Floor, Boston, MA  02110-1301  USA
 
