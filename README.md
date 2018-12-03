# arduino_4x4_cube
4 by 4 (by 4 technically) cube

# Construction
The cube is constructed with Cathode Layers and Anode columns.  If your construction is reverse i.e. Cathode columns and Anode layers, then you will need to change the code the following way:

All lines with `digitalWrite()` will need to be changed with 0's changed to 1's and vice-versa

Currently the code will be like

```c
digitalWrite(column[i], 0);
```

This means that currently this IO channel on the chip is on 'LOW' state i.e. 0 volts and in this state its acting as a 'Sink' and working like the ground.  Given our columns are Anodes, this means the LED will be in OFF state.

If you instead want it to be ON state, then change it to 

```c
digitalWrite(column[i], 1);
```

Instead.
