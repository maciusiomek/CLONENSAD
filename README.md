<center><h1>CLÖNENSAD</h1></center>
<h3>A cool looking 16x32 LED panel that works with WLED!</h3> 
I've made this project, because I just wanted to have something in my room that just shows my personality. 
I really liked Ikea OBEGRÄNSAD and especially <a href="https://github.com/ph1p/ikea-led-obegraensad">this hack</a> for it, but Ikea stopped producing them and it's really hard to get them on used markets. Because of that I've made this!
<br><br>
<img width="1000" height="auto" alt="image" src="https://github.com/user-attachments/assets/31a92f4e-36ff-4b62-b1e4-9d3eaa1d1d9c" />
<hr>
<h2>What you'll need to build this project and pricing.</h2>
You'll need a:<br>
  - PCBs - About $21 with shipping<br>
  - Like 3kg of filament (I'm using Elegoo PETG Pro) - About $40<br>
  - Super glue, T7000 or hot glue<br>
  - Lots of patience<br>
  - Screws - 25mm length, 3.5mm diameter, 8.2 mm head diameter - for me, they were free<br>
  - ESP32 C3 Zero - About $5 on aliexpress<br>
  - 512 WS2812 LEDs - The cheapest listing I found on aliexpress was about $18<br>
  - 12V PSU - I had one on had, it's about $30<br>
  - 12V to 5V converter - I'm using one from some company called TOBSUN, model EA75-5V. It worked great for the ambilight behind my monitor, so I think it's alr! - It was about $5-7<br>
<hr>
<h2>Assembly.</h2>
First, get your PCBs. You'll have to solder on 512 individual LEDs, I would recommend using a hot plate for this. Next, put them into your 3D printed panels. "OUT" should be looking the same way the arrow is on the image bellow. Put some hot glue onto the PCBs so they won't come off the panels. Now, solder everything together (+ goes to +, - goes to -, and "OUT" goes to "IN"). Basically just follow what's on the image bellow (this is a view from the back).
<br><br>
<img width="300" height="auto" alt="dupaaa" src="https://github.com/user-attachments/assets/15bf9591-b9e1-4e0d-9fc3-2a4cf81fa757" />
<br><br>
Connect it to your voltage converted in multiple places, I would recommend to solder in the power in every corner and in the center. Also adding a fuse is a great idea - I'm using a 15A fuse on 5V side. Now that the panel is basically done, lets move onto flashing WLED onto your ESP!<br><br><br>


Go to <a href="https://install.wled.me/">this site</a>. You should see something like on the image bellow. Connect your ESP, click install and choose something like "USB JTAG/serial debug unit". You should now have WLED installed!<br><br>
<img width="1000" height="auto" alt="image" src="https://github.com/user-attachments/assets/b4918559-d473-40b1-a899-763630b2476d" />
<br><br>
Go to the IP of your ESP and you should see something like bellow! Click on the "Config" button and then "LED & Hardware".<br><br>
<img width="1000" height="auto" alt="image" src="https://github.com/user-attachments/assets/56b17c35-f8a3-477e-8083-16c939b1e2d7" />
<br><br>
Set the max PSU current to 15A, set the length of your LED chain (512!) and the IO pin you're using - I choose 21! Click save and then click 2D configuration.<br><br><img width="1000" height="auto" alt="image" src="https://github.com/user-attachments/assets/f89b8a5d-5ee1-4c53-a956-066d4347058d" />
<br><br>
Set everything like on the image bellow!
<br><br>
<img width="1000" height="auto" alt="image" src="https://github.com/user-attachments/assets/00bda015-db4c-44c7-a5e0-4cffb8e1ee87" />
<br><br>
Now connect your ESP to the panel (5V, Data in to the pin you choose, GND) and you should be done! Choose the effect you want and click "Peek". The panel should show the same thing you can see on your screen!<br><br>
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/65a93615-dffb-4e1d-961a-3bb5f6f46359" />







