### 1.1 Information representations



**Denary:** 

- numbering system using base 10 (normal integer nu



**Binary:**

- number system using base 2
- values stored as a series of ones and series
- A singles 0 or 1 is called binary digit
- A group of 0 & 1 is called character

#### BCD (Binary Coded decimal) 

- Each digit in the number is written separately in a series of 4 bits
- why some bits can't represent BCD <fppmj13183civ>
  - each nibble can't contain any digit greater than 9
  - Digit must NOT be larger than 9
- **Used in**
  - when denary numbers need to be electronically coded
  - e.g. to operate displays on a calculator where each digit is represented 
  - decimal fractions can be accurately represented 
  - In business applications where each digit has to be retained in a result
  - Early computers store data and time in BIOS using BCD



#### Two’s compliments 

| 128(MSB) | 64   | 32   | 16   | 8    | 1 (LSB) |
| -------- | ---- | ---- | ---- | ---- | ------- |
| 1        | 0    | 1    | 1    | 1    | 1       |

Denary value = -128 + 32 + 16 + 8 + 4 + 2 = -66
Range = [-128] - [+127]



#### Character set <fppmj12184bi>

- The symbols that the computer recognises/uses 

- A list of characters recognised by the computer hardware and 

  software 



#### Explain the differences between the **ASCII** and **Unicode** character sets <fppmj12184bii>

- UNICODE has greater range of characters than ASCII 

- UNICODE represents most written languages in the world while ASCII 

  does not ASCII used for English only 

- ASCII uses 7 or 8 bits or one byte whereas UNICODE uses up to 4 

  bytes per character 

- UNICODE is standardised while ASCII is not 





#### 1.1.2 Image Representation

#### Bitmap image 

- made of pixels
- Each pixel has one color
- encoded by assigning a solid color to each pixel
- **Application**
  - Used to capture scanned images (from a paper document)
  - Used to scan a photo

#### How computer stores bitmap image

- Each pixel requires only one bit (as there are only two colours) 
- Black represented by 1 and white by 0 (or vice versa) 
- Bits are stored for each pixel in sequence 

#### Staircase effect 

- When overlarge a bitmap image, individual pixel may become **visible**

#### Pixel 

- Smallest picture element that can be drawn

#### File header 

- Stores data about the file contents/image/metadata <fppmj13186d>
- (such as image resolution, file size and color depth) <fppmj13186d>

#### Image resolution 

- Number of pixels per unit measurement

#### Screen resolution 

- The number of pixels which can be viewed horizontally and vertically

#### RLE (Run Length Encoding) 

- Lossless compression

- looks for runs of consecutive pixels of same colors

- Stores color and the number of it occurs

- For example B5

- **Lossless method of compression.** 

- Reduces (the physical size of) a string of adjacent, identical characters/pixels / bytes etc.. 

- The repeating string (a run) is encoded into two values. 

- One value represents the number of (identical) characters in the run (the run count). 

- The other value is the code of the character / colour code of pixel etc. in the run (the 

  run value). 

- The run value and run count combination may be preceded by a control character. 



#### How RLE encodes a bitmap image

![rle](/Users/Henz/Desktop/Screen%20Shot%202019-04-05%20at%2011.55.02%20AM.png/rle-4436898.png)

- 3B9 1A3 3B3 1A2 3B1 1A2 3B2 
- 1A1 3B3 1A1 3B2 1A2 3B1 1A2 3B3 1A3 3B9 

#### Color depth 

- Number of bits used to represent the color of a single pixel ?



|                        | 1 bit                                 | 2 bits   | 4 bits         | 8 bits           | 24 bits    |
| ---------------------- | ------------------------------------- | -------- | -------------- | ---------------- | ---------- |
| Des.                   | Monochrome<br/>(Black - 1, White - 0) | 4 colors | limited colors | Clos. to reality | True color |
| No. of color per pixel | 2^1 = 2                               | 2^2 = 4  | 2^4 = 16       | 2^8 = 256        | 2^24       |

#### Image size 

- Resolution        * Color depth
- [width * height] * [Ex. 4 bits]

#### Vector graphics

- Image defined using mathematics & geometry
- Objects and properties are stored mathematically
- **Resize without pixilation**
  - Image is recalculated with adjustment
- **Smaller file size**
  - Storing command, not individual pixels
- **Application**
  - Used in general line-drawing diagrams
  - Used in flowchart, object-oriented class diagram

#### Drawing list 

- set of commands used to define a vector



#### Graphic software

- **Resize** 
  - Increase / decrease the size of the image 
- **Crop** 
  - Remove part of the image 
- **Blur** 
  - Reduce the focus 



#### 1.1.3 Sound

#### ADC (Analogue to Digital Converter) 

- Converts analogue sound into digital signals which can be digitally stored

#### DAC (Analogue to Digital Converter) 

- Converts digit signals into analogue sound that can be  output

#### How sound is encoded 

- An analogue sound wave is picked up by a microphone
- sent to an ADC in the form of analogue electrical signals.
- Once the sound wave is converted into a digital form it can be stored and manipulated



#### How an analogue sound wave is sampled to convert it into digital format <fppmj12185a> <fppmj12164a>

- The height/amplitude of the (sound) wave is determined.
- At set (time) intervals // by example of sensible time period.
- To get an approximation of the sound wave
- And encoded as a sequence of binary numbers // and converted to a digital signal.
- Increasing the sampling rate will improve the accuracy of the recording.



#### Explain the effects of increasing the sampling resolution on the sound file <fppmj12185b>

- (Increasing the sampling resolution means) more bits per sample // larger range of values 
- Larger file size 
- More accurate representation of sound 



#### Explain the effect of decreasing the sample rate from 44.1kHz to 22.05kHz <fppmj12185c>

- Fewer samples (per unit time) 
- File size will decrease 
- Larger gaps / spaces between samples // Greater quantization errors 
- Sound accuracy will reduce // not as close to original sound 



#### How sound is represented 

- Sound is represented by wave forms
- The height of these waves can be sampled regularly with the height being represented by bit code

As samples are taken **more frequently**, quality will increase
As a **large number of bits** used to encode each sample, sound resolution **increases**

#### Sampling rate 

- No. of samples taken per unit time

#### Sampling resolution (bit depth) 

- Specified by the no. of bits used to encode the data for one sample

- or

- The number of distinct values available to encode/represent each 

  sample 

#### Bit rate 

- number of bits used to store 1s of sound
- Sampling rate * sampling resolution

#### File size of sound 

- Bit rate * length of sound

#### Features found in sound editing software 

- Cutting and pasting of sections of the recording
- Filtering out certain sounds. (For example the ‘click ‘ in vinyl record)
- Export sound recording to a variety of file formats
- Normalizing the recording level

#### Features of sound editing software <fppmj12185d>

- **Fading** 
  - Change the volume of a section of the sound for it get louder/quieter 
- **Removing sound / elements** 
  - Delete sections of the sound wave, for example, background noise 
- **Copy** 
  - Repeat elements of the sound wave 

#### 1.1.4 Video

#### frame rate (frame per second / FPS) 

- frequency at which the frames are displayed

#### Interlaced encoding (1080i) [NOT FULLY UNDERSTOOD] 

- Old technology
- Each filed display other horizontal line of the frame (double fps)
- frame rate * 2 = rate of picture display
- **adv**
  - refresh faster, save bandwidth & better smoothness
- **dis**
  - outdated & can’t show fast moving object clearly

#### Progressive encoding (780p) 

- Stores the data for an entire frame
- displays all the frame data at same time (gives more details)
- frame rate = picture displayed per second
- **adv**
  - Crisp, detailed frame
- dis
  - Rough frame transition

#### Inter-frame compression 

- remove neighboring frames which are similar
- some change in image is redundant
- how redundant the image between frames determines the amount of compression possible

#### Temporal redundancy (Inter-frame compression) 

- redundancy between frames
- correlation between two adjacent points

#### Spatial redundancy (Intra-frame compression) 

- redundancy within frame
- An inter coded frame that is divided in to macro blocks
- Blocks are not encoded with raw pixels values
- Encoded finds a block similar to the one in last frame (reference frame)
- BY ALGORITHMS

#### Multimedia container formats 

- Contains different type of data
- Audio | Video | codecs
- Video is compressed into codecs
- avi, mov, mp4, ogg

#### lossy compression 

- file accuracy is low, but files size smaller than lossless
- jpeg
- **based on 2 concepts**
  - encode image’s background pixels with a lower resolution
  - remove the colors which are less sensitive to human eyes (encode to a lower resolution)

#### lossless 

- reconstruct original data
- png





------



## 1.2 Communication and Internet technologies



NAT (Network Address Translation) ?11/o/n/18
Format of IPv6 (Valid or invalid) ?  11/o/n/18

#### Types of server

1. E-mail  server

2. file server

3. print server

4. web server

    



#### Client-server model 

- Types of computing system in which one workstation serves requests of other systems
- Server is generally most powerful computer in network
- Clients are individual components (which are connected in a network)

#### Client-side scripting

- The user’s web browser is the client software
- The requested web page has program code / script embedded within it
- This code is interpreted by the web browser 

#### Explain the difference between client-side scripting and server-side scripting <fppmj12186dii>

- Client-side (script) is run on the computer making the request (when the (web page) data is received by the computer) 
- Server-side (script) is run on the web server 
- The results are sent to the computer that made the request 

#### Applications of network 

- file server, Domain controller server, Email server, Printer server, Database server, web server

#### General process of client server model 

- Client computer makes a request to the appropriate server
- The processing of the request is carried out on the server
- The server packages the result in a form which is displayed by the client computer’s software

#### World Wide Web 

- collection of interlinked, hypertext documents/webpages/multimedia
- use https to transmit data
- web page written in html
- URL specify the location of the web page

#### Internet [Interconnected Networks] 

- Global system of interconnected networks
- uses TCP [Transmission control protocol] / IP protocol

#### Hypertext Transfer Protocol (HTTP) 

- a protocol to allow for the retrieval of linked resources from the across the WWW

#### URI (Uniform Resource Identifier) 

- a unique address for a resource on the WWW.

#### Transmission Control Protocol / Internet Protocol 

- communication language

#### Networks 

- LAN [local area network] : not over large geo area
- WAN [wide Area network]: formed by many  LAN connected together

#### Routers [Device that forwards packets of data between network using IP] 

- Used to connect multiple network segment
- Can route packets of same protocol over network with dissimilar archi. over the most efficient route

#### Gateway [device used to connect networks with different archi. and protocols.] 

- used between 2 LANS (able to convert the data packets from one portocol to another)

#### Server [Computer that run the server program] 

- serve request for users
- client connect to server through network

#### The Public Switched Telephone Network (PSTN) 

- Two-way voice communication
- All networks connected together by switching centers
- Allows any telephone to communication with another
- Dialup (Internet connection using PSTN)
- Data transferred using existing lines
- When data is being transmitted, the computer dials a network to set up a connection

#### Dedicated lines 

- A tele-communication line between computers, purchased from a telephone company
- adv
  - consistent data transfer speed
  - high and consistent bandwidth
  - fast upload speed
- features
  - carry phone cells
  - allow lots of staff to connect simultaneously
  - carry video transmission without buffering
- -

#### Cell phone network 

- Cell (wireless network spread over land area)
- each cell is served by at least one transceiver
- each feel uses a different set of frequencies to avoid interference
- when joined together, cells provide radio coverage over a wide geo area

#### Wireless 

- devices can be more mobile
- easy to set up
- connect to many different devices at the same time

#### Wired 

- Easier to hack
- Interference



#### Copper fiber

**Features**

- Can be twisted paired or co-axial

**Benefits**

- Flexible 
- Best conductor

**Drawbacks**

- Affected by electromagnetism 
- Expensive 



#### Fiber optic cable

**Features**

- Transmit light pulses

**Benefits**

- least likely to have interference
- Light weight
- More secure (difficult to hack)
- Greater bandwidth

**Drawbacks**

- Installation cost is high
- cable can break when bent
- only transmit data in one direction



#### Microwaves

**Features**

- [INCOMPLETE]

**Benefits**

- Wireless
- Larger bandwidth

**Drawbacks**

- '‘Emitting towers’ expensive to build
- Physical obstacles can interfere



#### Radio waves

**Features**

- wifi is an example of raio wave
- 

**Benefits**

- Large range of wavelengths
- Wireless transmissions

**Drawbacks**

- Low frequency so transmit less data at one time
- affected by radio stations with same frequencies



#### Satellite

**Features**

- [INCOMPLETE]

**Benefits**

- Large range of wavelengths
- Wireless transmissions

**Drawbacks**

- Easy to interfere
- Expensive to set up







#### Bit streaming 

- Bit stream is a sequence of bits
- represent a stream of bits
- transmitted continuously over a communication path
- serail (one at a time)

#### Real-time bit steaming 

- An event is captured on live
- Video signal is encoded to stream media files
- Encoded feed is then upload to file server
- Streaming servers duplicate the feed and send it to all clients

#### On-demand bit streaming 

- Videos is stored on a server as streaming media files
- If client requests to watch a specific video (a bit steam is set up which transmit the video)

#### Fast (broadband speed)/(bit rate) in bit streaming 

- clients have to download and display it at the same time
- higher quality, faster bit rate

#### Real-time streaming requires faster internet speeds BECAUSE

- GREATER number of users requesting the same data simultaneously

#### IP Address [Internet Protocol] 

- Numerical label assigned to each device (e.g. computer) participating in a computer network that uses the Internet Protocol
- used to ensure that message and data reach their correct destinations

#### function 

- allow device to send correct data to the destination
- locate a device on a network

#### IPv4 

- uses 32 bits (4 bytes)
- range from 0 -255
- separated by dots
- around 4 billion addresses
- Four numbers separated with ‘.’ 
- Each number is between 0 and 255 / 00 and FF in Hex / stored in one byte. 
- 32 bits long 

#### IPv6 

- uses 128 bits
- only one double colon(:) is allowed (15EF:5L63::2014:BB::60AA is invalid)

| Public IP                                                    | Private IP                                                   |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| Address provided to home network by ISP [Internet service provider] | address issued by router in home network                     |
| Address is unique through internet                           | address only unique in home network                          |
| Allows two diff. computers to identify each other            |                                                              |
|                                                              | NAT (Network Address Translation) is necessary for a private IP address to access the Internet directly. |
| Less secure                                                  | More secure                                                  |
|                                                              | range of private ip<br>10.0.0.1 to 10.255.255.254<br>172.16.0.1 to 172.31.255.254<br>192.168.0.1.to 192.168.255.254 |
|                                                              | can’t be accessed though the internet                        |



[NOT IN SYLLABUS]

|         | NetID | HostID | 1st Octect Range | Network Numbers            |
| ------- | ----- | ------ | ---------------- | -------------------------- |
| Class A | 1     | 2,3,4  | 1 to 126         | 1.0.0.0 to 126.0.0.0       |
| Class B | 1,2   | 3,4    | 128 to 191       | 128.0.0.0 to 191.255.0.0   |
| Class C | 1,2,3 | 4      | 192 to 223       | 192.0.0.0 to 223.255.255.0 |

#### Subnetting

- subnetting enables more efficient use of the network classess
- Subnet portion of the IP address
  - taken from the host portion
  - network portion never changes
- routers considers the network and the subnet portions when routing

[NOT IN SYLLABUS]

#### Uniform Resource Locator (URL) 

- a character string referring to the location of an internet resource

#### Domain name 

- humaly-memorable names for internet components (computers and network)
- One domain name can be connected to multiple IP addresses

#### Domain Name Service (DNS) 

- naming systems for computer having internet connection

#### Client side scripting 

- The user’s web browser is the client software
- The requested web page has program code (Interpreted by web browser)
- Used to
- enables web pages to be scripted
- allow user input to change the content
- -

#### Server side scripting 

- code that runs on server written using server language.
- Used to
- provide interface for client
- limit client access to database

#### Client server 

- File is available from FTP server
- User’s browser is the client software
- Client request file from server

#### How a user opens a web page 

1. Browser parses the URL to obtain the Domain Name
2. Then passes the Domain Name to DNS
3. DNS stores list of Domain Name and IP address
4. DNS Name resolver looks for DN in its database
5. **IF Found** -> Return the IP address to the originator
6. **Else**  -> Forward to higher level DNS
7. Original DNS returns the IP address to the originator
8. Browser used the returned IP to request web page FROM WEB SERVER
9. Web server retrieves the page to originator
10. Browser interprets the the scripts and display it.



## 1.3 Hardware

#### 1.3.1 Input Devices

**Keyboard:** 

- device used to input text into a computer system. 
- When a key is pressed, an electrical circuit is completed. 
- Circuit transmits a binary signal to computer, using ASCII code which represent the key pressed. 

**?Trackerball mouse:** 

- pointing device consisting of a ball held by a socket containing sensors to detect a rotation of the ball about two axes. 

**Laser mouse:** 

- pointing device which uses a red LED to illuminate the surface
- the CMOS sensor sends image that is reflected back to a digital signal processor(DSP) for processing
- DSP detect patterns of images to determine the movement of the mouse
- Coordinates are sent back to the computer

**Flatbed scanner:** 

- optically scans documents, & converts it to a digital image. 
- Composed of a glass pane, bright light which illuminates pane and a moving optical array. 

**Sensor:** 

- device that detects events or changes in physical quantities and provides a corresponding output, generally as an electrical or optical signal 



#### Resistive screen

- consists of two charged plates 
- Pressure causes the plates to touch 
- Completing the circuit 
- Point of contact registered 
- Coordinates used to calculate the position 



#### Capacitive screen

- made from materials that store electric charge 
- When touched charge transferred to the finger 
- Sensors at the (screen) corners detect the change 
- Point of contact registered 
- Coordinates used to calculate the position 



#### Optical Mouse 

1. It has Led acts like camera
2. Led bounces light off the surface onto the CMOS
3. LED light is reflected back to CMOS*
4. CMOS sends each image to DSP*.
5. DSP detects the pattern from the analysis of the image – return to computer

#### keyboard 

- Uses switches and circuits to translate keystrokes into signals the computer can understand
- when user press a key, a circuit is complete
- processor compares location of signal of the key pressed with the data in rom

#### optical disc 

- a lens focused the laser onto the disc
- laser beam is shone onto disc to read file
- reflected beam is then encoded as bit pattern

#### scanner 

- laser beam is shone onto the source docuement
- then the reflected beam reaches the sensitive diode by mirrors
- sensors detect level of reflected light
- light intensity is converted to electrical signal

#### Microphone 

1. Sound vibration hits diaphragm
2. Diaphragm [movement] causes coil to move
3. Coil [movement] induces a current
4. Electrical current is digitized
5. Digital content is played back using software

#### 3.2 Output Devices

**Actuator:** 

- type of motor that is responsible for moving or controlling a mechanism or system through which a control system acts upon an environment. 

##### Non-impact printer

- A printer without banging a ribbon onto paper

##### Printer:

- output device that makes a persistent readable representation of graphics/text on physical media.

##### Laser printer 

- Non-impact printer
- Page printer

1. A laser beam and a rotating mirror are used to draw an image of the page on photosensitive drum.
2. The image is converted into electrostatic Charge on drum
3. Ele. charge attracts toner
4. Charged paper is rolled against drum
5. Opposite charge paper picks up toner particles from drum
6. Paper passes through fuser (heats up paper)
7. Toner melts and forms permanent img on paper.
8. Charge is removed from the drum





##### Inkjet printer

- Non-impact printer
- Line printer
- work by propelling variably-sized droplets of liquid or molten material (ink) onto physical media

1. Print head of the printer contains nozzles (fed ink from cartridge)
2. The print head (connected by belt to a motor) move across the paper..
3. The head drops tiny droplet of ink

##### Print head 

- The print head contains a large number of very small nozzles
- Ink is fed to each nozzle from a reservoir
- The print head fires droplets of ink onto the paper
- The print head moves horizontally across the paper
- **Second**
  - Tiny resistors create heat inside each nozzle
  - The heat vaporises ink to create a bubble
  - When the bubble pops the ink is deposited on the page 
  - The collapsing bubble creates a partial vacuum in the nozzle 
  - And ink is drawn from the reservoir ready for printing the next dot
- **Third:** 
  - There is a piezo crystal at the back of the ink reservoir of each nozzle 
  - The crystal vibrates when it receives a tiny electric charge 
  - Ink is forced out of the nozzle by the inward vibration 
  - The outward vibration creates a partial vacuum in the nozzle 
  - Replacement ink is pulled into the reservoir 

##### Stepper motor 

- The (print head) stepper motor is connected to the print head by a belt
- The (print head) stepper motor moves the print head across the paper
- The (parking) stepper motor parks the print head assembly when not in use
- The (paper feed) stepper motor turns the rollers that provide the paper feed // The (paper feed)stepper motor moves the paper in small increments 



#### Speaker

- Takes electrical signal and translates into physical vibrations to create sound waves;

#### parts: 

Diaphragm
Coil
Magnet
Suspension

1. Elctric current in current creates electro-magnet field
2. Change in audio signal causes the electric current [direction] to change
3. Current [directions] determines electromagnet [polarity]
4. Electro-magnet is attracted or repelled by the permanent magnet
5. Cause magnet to move
6. Coil [movement] causes cone vibrates
7. Vibration is transmitted into the air



#### 1.3.3 Secondary storage

**Optical disks:** 

- flat, usually circular disc which encodes binary data in form of pits and lands. 
- Pits = 0, due to lack of reflection and lands 
- = 1, due to reflection when read 

**Hard disk drive:** 

- data storage device consisting of rotating disks, platters, with magnetic heads arranged on an actuator arm to read and write data to the surfaces. 
- Platters are made of aluminium/glass
- Surfaces of the platter are magnetised
- Disks are rotated at high speed
- Inexpensive per unit of storage
- Larger storage capacity than flash drive

**DVD-RAM**

- data is stored/written using lasers/optical media 

- DVD-RAM uses phase changing recording, in which varying laser intensities cause 

  targeted areas in the phase change recording layer to alternate between an amorphous 

  and a crystalline state. 

- uses a rotating disk with concentric tracks 

- allows read and write operation to occur simultaneously 

**Flash memory / pen drive:** 

- most are NAND-based flash memory 

- there are no moving parts 

- uses a grid of columns and rows that has two transistors at each intersection 

- one transistor is called a floating gate 

- the second transistor is called the control gate 

- memory cells store voltages which can represent either a 0 or a 1 

- essentially the movement of electrons is controlled to read/write 

- not possible to over-write existing data; it is necessary to first erase the old data then 

  write the new data in the same location 

#### RAM (Random access memory)

- Store data during computer running
- Read & write data
- Volatile (data gone when computer is off)

#### ROM (Read Only Memory)

- Store boot up instruction / OS Kernel <fppmj13187d>
- Only read data
- Non-volatile

#### Need for secondary storage 

- ram is volatile and rom is non-editable
- need for permanent and non-volatile storage



#### Static Ram 

- 6 to 8 transistors
- more complex circuitry
- does not need to be refreshed as the circuit holds the data aslong as the power supply is on
- used predominantly in cache memory of processors where speed is important
- **adv**
  - More space in chip
  - Faster data access time
  - requires less power
- **dis**
  - 4 times expensive
  - Lower storage capacity

#### Dynamic Ram 

- single transistor
- requires data to be refreshed periodically in order to retain the 
- requires higher powerconsumption which issignificant when used in battery-powered devices
- **adv**
  - less expensive to produce
  - higher storage capacity
  - less complex in circuit
- dis
  - slower access
  - requires more power

#### Intergrated Circuit 

- set of electronic circuit on one small plate (“chip”) of semiconductor material



## 1.4 Processor fundamentals



#### Von Neuman Architecture 

- Uses single processor
- follows a linear sequence of fetch-decode-execute cycle (for the set of instructions)
- by using registers

#### Register 

- Small piece / word of (fast) memory 
- Part of the processor 
- Temporary storage of data 
- Data is about to be / has been processed 

#### General Purpose Register 

- One or more registers in the CPU that temporarily store data
- normally eight of this in microprocessor
- can be used by the assembly program

#### Special Purpose Register 

- some are accessible by assembly program
- some are not accessible

#### Program Counter (IN CU) 

- Store the address <fppmj13183b>
- of the next instruction to be fetched <fppmj13183b>
- so that the next copy of instruction can be placed in CIR

#### MDR (Memory Data Register) 

- Stores / holds data / instruction when fetched from memory 

- Stores / holds data which is being written to memory 

- The location accessed is the address held in the Memory Address 

  Register (MAR) 

#### MAR (Memory Address Register)  (IN CU)

- used to hold the memory address that contains either
- the next piece of data OR
- an instruction that will be used

#### Index Register 

- Used if the address is indirect
- stores a number which will be used to change an operand address
- a constant from the instruction added to IR to form a new address (to data)

#### Current Instruction Register  (IN CU) 

- holds the instruction that is to be executed

#### Status Register 

- is interpreted as independent bits <fppmj13183b>
- each flag is used to determine where or not some event has occurred<fppmj13183b>

#### Accumulator  (IN ALU) 

- single general purpose register (inside ALU)
- values are hold in this when processed by Arithmetic & Logical Comparison

Processor

#### Arithmetic and Logical Unit (ALU) 

- performs arithmetic calculations & logical decisions<fppmj13183b>
- Arithmetic operations: add, subtract, multiply etc.
- Logical operations: comparing binary patterns and making decisions

#### Control Unit (CU) 

- send and receive signal<fppmj13183b>
- Synchronise operation (to control operation)<fppmj13183b>

#### System Clock 

- timing device
- connect to the processor
- that synchronize when fe cycle runs

#### Bus 

- set of parallel wires that connect various components
- & provide communication between them

#### Data bus 

- Bi-directional
- carry data between system components
- MDR is one end of data bus

#### Address bus 

- unidirectional
- carries main memory[address] or i/o device about to be used
- from processor to MAR

#### Control bus 

- bi-directional
- send control signal
- from CU to ensure [(use of data) & (address bus used by components)] doesn’t lead conflicts

#### Bus width 

- determined the mac possible memory capacity of the system
- Wider bus -> more bits can be transferred simultaneously

#### Clock speed 

- number of cycles (performed by CPU) per second
- faster clock speed means fe cycle faster
- also causes processor to heat up

#### Ports 

#### Peripheral devices 

- hardware devices outside the CPU
- can’t directly connect to processor
- processor connect to i/o by i/o controller

#### I/O Controller 

- electronic circuit board consisting of:
- interface allowing connection of controller to system
- set of data, command and status registers
- I/O Port {
- provide physical interface between the computer and a device

- need of I/O Port {
- allows I/O devices to be connected to CPU without having specialized hardware for each one
- USB port can connect to many different I/O

#### Fetch Execute Decode Cycle 

- **The fetch stage:**
  - Copy the address that is in the PC into the MAR
  - Increment the PC (ready for the next fetch)
  - Load the instruction in address of MAR into the MDR
  - Load the instruction in MDR into the CIR
- **The decode stage:**
  - Identify type of addressing used by instruction
  - Direct address: load copy into MAR & retrieve data
  - Indirect address: add address to IR, copy result to MAR o Retrieve contents of new address
  - Decode the instruction
- **The execute stage:**
  - If instruction == jump instruction
  - load address operand into PC then go to start
  - If not
  - execute the instruction then go to start

#### Register Transfer Notation (RTN) 

MAR <- [PC]
PC  <- [PC] + 1
MDR <- [[MAR]]
CIR <- [MDR]
DECODE
EXECUTE
RETURN TO START
Single bracket == value stored in that register
Double bracket == value obtained by logical process by CPU

#### Interrupts 

- a signal from some devices seeking the attention of the processor
- Interrupt register
- before each cycle, the interrupt register is checked
- IF priority
- current running process is saved
- control of the processor is given to interrupt handler

#### Interrupt handler (Interrupt Service Routine) 

- different ISR are used for different types of interrupt
  Sequence of interrupt handling
- Current fetch-execute cycle completed
- Contents of all registers, especially PC, stored away
- Source of interrupt identified
- If low priority:
  - then disabled
- If high priority:
  - PC loaded with address of relevant ISR
- ISR executed
- All registers except for PC are restored to original
- Interrupts re-enabled
- PC is then restored
- Return to start of cycle

#### Human understandble way:

- At the end of the cycle for the current instruction the processor checks if there is an interrupt. 
- If the interrupt flag is set, the register contents are saved, 
- the address of the Interrupt Service Routine (ISR) is loaded to the Program Counter (PC) and when the ISR completes, 
- the processor restores the register contents.
  The interrupted program continues its execution.

### 1.4.11 Addressing

#### Maximum number of memory locations in denary of 8-bit operand

- 256 (zero is counted)



#### Direct addressing 

- Load the address[content]
- **what happens when LDD 35 is executed**
  - the MAR is loaded with the operand of the instruction // loaded with 35 
  - the Accumulator is loaded with the contents of the address held in MAR
    // the Accumulator is loaded with the contents of the address 35 

#### Indirect addressing

- Load the address [content] - > [content]

#### Immediate addressing 

- Load the number

#### Indexed addressing 

- The address + the val in IR (Index Register)

- The contents of the index register are added to operand to give the actual 

  address 

Symbolic addressing [COMPLETELY NOT UNDERSTOOD]

#### Relative addressing 

- Next instruction is the an offset number of locations away (for example, jpe, jnp)

- A number (the offset) is added to the base address to give the actual 

  address 

#### Conditional jump 

- has a condition that will be checked (like if)

#### Unconditional jump 

- no conditional check
- just go to next one

#### Assembly language 

- Low-level
- Made of instruction (opcode and oprand)

#### Machine Code 

- In binary
- Uses processor [basic operation]

#### Assembly language  <[Relationship]> Machine code  

- every assembly instruction translated to a machine instruction (1 to 1)

#### Symbolic addressing 

- Mnemonics used to represent operation code
- labels can be used for address (PRICE = 232)

#### Absolute addressing 

- A fixed address in memory

#### Assembly directives [NOT FULLY UNDERSTOOD] 

- the information that the assembler translate software needs to be able to translate the source code
- used to specify:
- starting address for programs
- staring value for memory locations
- the end the program text

#### Macros 

- like [function] in Js
- a name assigned to a group of instructions
- can be used anywhere in the program
- can be expanded to a group of instructions

#### Assembler 

- Assembly language to machine code
- replaces all mnemonics and labels with their respective binary values
- the binary values are predefined before the assembler software

##### Directive

- an instruction to the assembler program
- (how the assembler should construct the final executable machine code, for example like how memory should be used)
- 

#### One pass assembler 

- converts mnemonics source code into machine code (in a sweep of program)
- can’t handle code involving forward referencing

#### Two pass assembler [NOT FULLY UNSERSTOOD, ESPECIALLY THE ONE WITH THE CHART] 

**first pass**

- symbol table created to enter symbolic address & labels into specific address
- all errors are suppressed

**second pass**

- jump instructions can access memory address from the table
- whole source translated into machine code
- error reported if they exist



## 1.5 System software



#### 1.5.1 Operating system 

- A set of programs designed to run in the background on a computer
  - Controls operation of computer system
  - Provides a user interface 
  - Controls how computer responds to user’s requests
  - Controls how hardware communicate with each other
  - Provides an environment in which application software can be executed 



DESCRIBE THE WAYS IN WHICH OS HIDES THE COMPLEXITIES OF HARDWARE [NOT UNDERSTOOD]

#### Why operating system is needed [Exam focus]

- Hardware is unusable without an OS
- Acts as user interface between user and hardware
- Provides software platform / environment on which other programs can be run 

#### Management task 

- **Processor magement :** 

  - for multiprogramming (decide which job wil get to next use of processor)
- **File management :** 
  - Storage space divided into file allocation units <fppmj12181ai>
  - Create directory structure  <fppsmj12181ai>
  - provide file naming conventions  <fppsmj12181ai>
  - implement password protection  <fppsmj12181ai>
- **Input / Output management :** 

  - control all input and output
- **Main memory management :** 
  - Allocates RAM to program
  - Handles virtual memory
  - Memory protection (prevents a processor accessing memory not allocated to it)
- **Provide HCI (Human Computer Interface ) :** 

  - Controls communications between users and hardware
- **Process management**
- **Security management:** 
  - Set up user accounts
  - Authentication (Checks username, accounts)
  - Automatic backup
- **State three printer management tasks that OS performs **<fppmj12181aii>
  - Installs printer driver 
  - Sends data to the printer 
  - Sends commands to printer 
  - Receives and handles interrupts from the printers

- **Interrupt handling**
  - Identifies priorities of interrupts
  - Saves data on power outage
  - Loads appropriate Interrupt Service Routine (ISR)

  



### 1.5.2 Utility program

#### Utilities 

- system software designed to analyze, configure, optimize computer
- allow maintenance to be done



#### Utility software 

- **library program** is not

- **File compression software** 
  - When computer runs out of space
- **Backup** 
  - When user lost data or files
- **Disk repair software** / Disk content analysis
  - When disk repair report ‘Bad’ sector errors
- **Anti-virus software**
- **Disk defragmenting software** 
  - Organise small piece data, reorganize storage on disk
- **System clean up**
- **Automatic update** 
- **Disk formatter** 
- **Firewall**

#### Disk formatter 

- carries out a process for preparing the data storage device for storing
- Formatting, process where the computer ‘draw lines’ on the surface of disk to split into small areas

#### Virus checker 

- finds and removes computer viruses from a computer
- Virus checker keeps a constant check on files, searching them and deleting
- When files sent from one computer to another computer , (it may contains virus that harms the computer)

#### Defragmenter software 

- Reorganizes files & unused spaces on computer (so access faster)
- Big file (store in multiple sections)
- Fragmentation
- contents of a file are scattered across two or more sectors
- slows down disk access and performance of computer
- Defragmenting files: reorganizes files so they are stored in contiguous sections

#### Disk content analysis 

- for visualization of disk space usage
- record size of each file and generate a graph showing disk usage

#### File compression 

- reduce the size of file by cutting the duplication of data in file
- improve computer performance by reducing the data that needs to be stored

#### Automatic backup 

- Duplicate important data in the event of hard drive failure, user error.
- Used for individual or enterprise
- Can be set to backup on schedule by user

### 1.5.3 Library Program 

- Collection of resources used to develop softwares

- Made of pre-written code (functions)

- Provide services to other more complex program

- **adv**

  - less time consuming
  - reduce need for testing
  - better engines

- **dis**

  - Prone to viruses
  - may require manual tweak

  

#### E.g. of LP 

- design of program on Win7{
- all program use Windows GUI Library
- gives a uniform experience

#### Dynamic Link Library (DLL) 

- a shared library file
- code is saved separately from .exe file
- only load code to main memory during run-time
- can be used by different programs running simultaneously (therefore reduce strain on memory)
- DLL can be seen as a module for complex program (therefore easier to install and run update)
- adv
  - .exe file is smaller (dll only load to main memory when needed)
  - dll code can be modified independently, no need to recompile the whole file

#### Library routine 

- pre-existing code which can be used by programs <fpp>
- to perform complex task <fpp>
- **adv**
  - less code to be written -> save time <fpp>
  - pre-tested -> reduced time testing <fpp>
  - simplifies the program -> since just the name of function is included <fpp>
- **dis**
  - compatibility issue -> may not work in other code <fpp>
  - may not meet needs -> may give unexpected results <fpp>
  - if library routine is changed -> there may be unexpected results <fpp>

#### Assembler

- Translates assembly language into machine code
- The mnemonics used translates into machine opcodes
- Process simple because assembly language has a one-to-one relationship with machine code.
- Assembler basically translate mnemonics into binary 



#### Compiler : 

- High level to low level
- The compiled program can be independently distributed. 
- Compiler reports all errors at the end of compilation 
- a compiler checks the whole program for errors 
- Cross-compilation is possible/compile on one hardware platform to run on another. 
- Create an .exe file (which doesn’t need compiler software)
- **adv**
  - .exe easily distributed 
  - With .exe, don’t need compiler software 
  - No source code – users not able to edit/plagiarize 

- **dis**

  - Only be produced when all errors are fixed
  - Development process long – locating errors
  - Uses a lot of resources

  

#### Interpreter 

- High level to low level
- Line by line
- Debugging easier / faster
- an interpreter stops when it reaches an error. 
- Interpreter executes each statement immediately after decoding 
- The interpreter software/source code must be present in main memory every time the program is executed 
- **adv**
  - Can run program any time, even before code finished 
  - Debugging easier/faster 
- **dis**
  - Execution very slow
  - translated each time run 
  - Interpreter needed
  - No .exe produced 

#### Machine independent 

- Program can be translated to run any platform
- Source code is translated to machine independent intermediate code

#### Java 

- A machine independent language
  How it’s translated
- Uses two-step compilation process
- Partially interpreted partially compiled
- Java source code is compiled to ‘bytecode’ by java compiler
- ‘bytecode’ is finally interpreted by **JVM** (Java Virtual Machine)





## 1.6 Security, privacy and data integrity

**Data security:** making sure that data is protected against loss and unauthorized access.

**Data integrity:** making sure that the data is consistent / accurate <fppmj13182b>

**Privacy of Data:** deals with the ability to determine what
data is shared with the third party

| Security                                       | Integrity                                                    |
| ---------------------------------------------- | ------------------------------------------------------------ |
| keeping the data safe.                         | making sure that the data is correct / valid.                |
| the prevention of data loss and illegal access | ensures that the data received is the same as the data sent / data copied is the same as the original. |



#### 1.6.1 Security of Data and Computer System

| Security of data                                             | Security of system                                           |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| Protection of **data** on a computer system                  | Protection of the **computer system**                        |
| To prevent corruption of data and prevent hackers from using data | To prevent access of viruses to the system and prevent hackers to enter your computer system |
| E.g. encryption                                              | E.g. ID & Password                                           |

#### 1.6.2 Security Measures for Computer Systems

- **User Accounts:**
  - Each user has an ID and password which are the log in details for a his user account
  - User assigned privilege which gives him access to only his workspace, preventing him to have admin rights.
  - Can assign privilege to files so users with low privileges do not have access. 
- **Firewalls**:
  - Set of programs, located at network gateway, that protects the resources of a private network from users from other networks
  - Filters information incoming to computer system
  - Information packets can be flagged by firewall and thus not allowed through
  - sits between the computer or LAN and the Internet/WAN and permits or blocks traffic to/from the network 
  - can be software and/or hardware 
  - software firewall can make precise decisions about what to allow or block as it can detect illegal attempts by specific software to connect to Internet 
  - can help to block hacking or viruses reaching a computer 
- **Authentication techniques:**
  - Digital signatures: a unique personal trait required bya computer to access certain data
  - Password: case-sensitive, unique string of letters, numbers and special characters.
  - Biometric scans e.g. retina, fingerprint, palm
  - process of determining whether somebody/something is who/what they claim to be 
  - frequently done through log on passwords/biometrics 
  - because passwords can be stolen/cracked, digital certification is used 
  - helps to prevent unauthorised access to data 

#### 1.6.3 Security Measures for Data

**Data backup:** an exact copy of an original piece of data in case the original is lost or corrupted

- Can be made on any type of storage device
- May be within the same computer system or at a
  different site
- 

**Disk-mirroring strategy:** real-time strategy that writes data to two or more disks at the same time.

- If one fails the other is still there to be read off of
- It can be done using more than one extra hard disk



**Encryption:** conversion of data to code by encoding it

- Data stored in an incomprehensive state
- Doesn’t prevent illegal access but appears meaningless
- Necessary to use decryption software to decode data
- Encryption keys complex algorithms; cannot crack



**Access rights to data (authorization): **

- different users are assigned different authorization levels which prevent them from accessing all the data so increase security

##### Ways of DBMS software to ensure the security

- Issue usernames and passwords...
  - stops unauthorised access to the data
  - any further expansion e.g. strong passwords / passwords should be changed regularly etc...

- Access rights / privileges...
  - so that only relevant staff / certain usernames can read/edit certain parts of the data
  - can be read only, or full access / read, write and delete
  - any relevant example e.g. only class tutors can edit details of pupils in their tutor group
- Create (regular / scheduled) backups...
  - in case of loss/damage to the live data a copy is available
  - any relevant example e.g. backing up the attendance registers at the end of each day and storing the data off-site/to a separate device
- Encryption of data...
  - if there is unauthorised access to the data it cannot be understood // needs a decryption key
  - any relevant example e.g. personal details of pupils are encrypted before being sent over the Internet to examination boards
- Definition of different views...
  - composed of one or more tables
  - controls the scope of the data accessible to authorised users o any relevant example e.g. teachers can only see their classes
- Usage monitoring / logging of activity...
  - creation of an audit /activity log
  - records the use of the data in the database / records operations performed by all users / all access to the data
  - any relevant example, e.g. Track who changed a student’s grade

#### 1.6.4 Errors that can occur 

- **Errors on input**
  - data keyed wrongly (a batch of data can be lost OR enter them twice)
- **Errors in operating procedure**
  - update master fie twice
- **Program errors**
  - lead to corruption, may be detected after a while
- **Viruses**
  - files can be corrupted or deleted by virus
- Transmission error
  - interference can occur in transmitting and receiving data (therefore data received wrongly)

#### 1.6.5 Data validation 

checks data entered is sensible

- **Range check:** data must be between a set of values
- **Type check:** data must have correct character type
- **Format check:** data must follow correct pattern/order
- **Length check**: data must have an exact no. of characters
- **Existence check:** data entered must exist (e.g. barcode must correlate to an item)
- **Presence check**
  - to ensure it is not empty
- **Uniqueness check**
  - To ensure no two runners have the same number
- **Check digit:** 1 digit is used to be answer to an arithmetic
  operation of other digits in data. If not matched then data entered incorrectly

***Data can be valid but this doesn’t mean data is accurate***



#### 1.6.6 Data Verification for Data Entry

**Data verification:** checks data entered is accurate

- Person manually compares original data with that entered to check if correct
- Enter data into computer twice and compares.
- If differences found, go back to raw data to fix error 

#### 1.6.7 Data Verification during Data Transfer

Errors may occur when data moved from one point to another point in system. Following find errors:

- **Parity Check:**
  - All data transmitted as bits
  - Number of 1s in a byte must always be either an odd number or an even number
  - **Example:** two communicating devices decide there will always be an odd number of 1s. A byte is received that has an even number of 1s so error must have occurred and receiving device would ask for it to be sent again
  - Used also when data sent between parts of the CPU
  - **dis**
    - Not foolproof: if 2 errors made, data accepted 
  - **futher check**
    - A parity bit is worked out for each column
    - The computer checks the parity of each bit position in parity byte
    - If incorrect parity then there is an error in the data received 
    - The position of the incorrect bit can be determined 
- **Checksum Check:**
  - Data sent from one place to another as block of bytes rather than individual bytes
  - Computer adds together all bytes being sent
  - Any bits lost at most-significant end as carry ignored so answer is an 8 bit number
  - Checksum calculated before and after data sent
  - If two bytes different, error occurred therefore block of
    bytes must be sent again
  - 
- **Proof reading**
- **Double entry**
- **Hash total** 
  - Total of several fields of data 
  - Including fields not usually used in calculations 
  - The result is transmitted with the data 
  - Calculation repeated at receiving end 
  - Results compared 
  - If different an error has occurred 



## 1.7 Ethics and ownership

**Computer Ethics**: how computing professionals should make decisions regarding professional & social conduct. 



#### 1.7.1 ACM/IEEE Software Engineering Code of Ethics

**Eight ethics principles of software engineers (SEs):** 

1. **Public**: act consistently in the public interest
2. **Client and employer:** act in the best interests of client and act in the best interests of employer 
3. **Product:** software and related modifications meet highest possible standards 
4. **Judgment:** maintain integrity and independence in their professional judgment 
5. **Management:** team leaders should subscribe to and promote an ethical approach to the management of software development and maintenance. 
6. **Profession:** advance integrity & reputation of profession 
7. **Colleague:** be fair to & supportive of colleagues 
8. **Self:** participate in lifelong learning regarding practice of 



#### 1.7.2 Ownership 

**Data ownership:** having legal rights and complete control over a single piece or set of data elements. 

- **Copyright** gives the creators of some types of media rights to control how they're used and distributed. 
- Programming ideas and methods can be stolen by competitors, software can easily be copied and bootlegged (sold illegally) hence **legislation** is needed to protect the ownership, usage and copy right of data. 

#### 1.7.2 Software Licensing

**Free Software Foundation:** 

- License gives user freedom to run, copy, distribute, study, change and improve software.
- Condition: any redistributed version of software must be distributed with original terms of free use, modification, and distribution (aka copyleft) 

**The Open Source Initiative:** 

- Source code of an open-source software is readily available to users under a copyright; does not enable user to re-distribute the software 
- Concept of open-source program relies on fact that a user can review a source-code for eliminating bugs in it 
- The source code comes with the software. <fppmj13163a>
- The user can edit the source code. <fppmj13163a>
- Once edited, the software is re-distributed with the changes. <fppmj13163a>

**Shareware:** 

- Demonstration software that is distributed for free but for a specific evaluation period only 
- Distributed on trial basis and with an understanding that sometime later a user may be interested in paying for it 
- Used for marketing purposes

**Commercial:**  <fppmj13163b>

- Requires payment before it can be used, but includes all program's features, with no restrictions 
- The software is purchased. 
- With a licence which restricts the number of users / possible time period for use. 
- The program code for the software cannot be edited. 
- **benefit of choosing commercial software option **<fppmj13163c>
  - Support / training is readily available so help can be accessed if needed. 
  - More robust software / fewer bugs as it has been tested more thoroughly/by more users. 
  - Forums / user groups will exist for popular software. 
  - Software upgrade path likely to be available (at minimal cost). 
  - Manufacturer develops patches that can be automatically downloaded. 
  - Compatibility is inbuilt for other commercial software. 





## 1.8 Database



#### Spreadsheet 

- Data stored in discrete files, stored on computer, and can be accessed, altered or removed by the user
- **advantage:**
  - Easy to search
  - Cheap
  - No skills
- Disadvantage:
  - Repeated data in different files
  - Impossible for multi-users
  - Sorting must be done manually
  - Data may be in different format (difficult to find and use)

#### Adv of relational database 

- reduced data redundancy (data is stored in linked tables)
- security is improved (differnt users have different access rights)
- complex queries can be written (to search specific data in the table)

##### Database  

- Collection of non-redundant interrelated data

##### Database management systems 

- Software programs that allows database to be defined, constructed or manipulated

##### Features 

- **Data management:** 

  - data stored in relational databases (tables stored in secondary storage)

- **Data dictionary** 

  - A file or table containing all the details of the database design

  - List of all files in database
  - No. of record in each file
  - Name & types of each field

- **Data modeling:** 

  - analysis of data objects used in database, identifying relationships among them

- **Logical schema:** 

  - overall view of entire database, includes: entities, attributes and relationships

- **Data integrity:**

  - entire block copied to user’s area when being changed, saved back when done
  - data design features to ensure the validity of data in the database

- **Data security**

  - handles password allocation
  - verification
  - backups database automatically
  - controls what certain user’s view by access rights of individuals or groups of user



##### Data change clash solutions:

- Open entire database in **exclusive mode** – impractical with several users
- **Lock all records** in the table being modified – one user changing a table, others can only read table
- **Lock record** currently being edited – as someone changes something, others can only read record
- User specifies **no locks** – software warns user of simultaneous change, resolve manually
- Deadlock**:** 2 locks at the same time, DBMS must recognize, 1 user must abort task 

##### Database VS file-based approach

- By storing data in (separate) linked tables data redundancy is reduced / data duplication is controlled... 
- Compatibility / data integrity issues are reduced as data only needs to be updated once / is only stored once. 
- Unwanted or accidental deletion of linked data is prevented as the DBMS will flag an error. 
- Program - data dependence is overcome. 
- Changes made to the structure of the data have little effect on existing programs. 
- Ad-hoc / complex queries can be more easily made as the DBMS will have a query language/ QBE form. 
- Unproductive maintenance is eliminated as changes only need to be made once (rather than changing multiple programs). 
- Fields can be added or removed without any effect on existing programs (that do not use these fields). 
- Security / privacy of the data is improved as each application only has access to the fields it needs. 
- There is better control of data integrity as the DBMS (uses its Data Dictionary) to perform validation checks on data entered.



**Tools in a DBMS:**

- **Developer interface:** 
  - allows creating and manipulating database in SQL rather than graphically
- **Query processor:** 
  - handles high-level queries. 
  - It parses, validates, optimizes, and compiles or interprets a query which results in the query plan. 



#### 1.8.3 Relational Database modelling

**Entity:** 

- object/event which can be distinctly identified 

**Table:** 

- contains a group of related entities in rows and columns called an entity set

**Tuple:** 

- a row or a record in a relation

**Attribute:**

- a field or column in a relation 

**Primary key:**

- attribute or combination of them that uniquely define each tuple in relation 

**Candidate key**: 

- attribute that can potentially be a primary key 

**Foreign key:** 

- attribute or combination of them that relates 2 different tables 

**Referential integrity:** <fppmj12187b>

- Prevent referencing data that does not exist

- Cascading update, delete

  - A primary key cannot be deleted unless all dependent records are already deleted  

- Cascading update / edit 

  - A primary key cannot be updated unless all dependent records are already updated 

- Every foreign key value has a matching value in the corresponding 

  primary key 

- The foreign keys must be the same data type as the corresponding 

  primary key 

**Secondary key:** 

- candidate keys not chosen as the primary key 
- User may frequently want to search on that field (example contact name)
- Allows for faster search using contact name

**Indexing:** 

- creating a secondary key on an attribute to provide fast access when searching on that attribute; indexing data must be updated when table data changes 



### 1.8.5 Normalization

##### Aim of normalizaiton

- to make the database more efficient by removing as much redundant and unnecessary repeating data as possible

**1st Normal Form (1NF):** <fppmj12187c>

- **No repeated groups of attributes, no duplicated rows**
- All attributes should be atomic (data item cannot be broken doen any further)
- each row is unique and has a unique name

**2nd Normal Form (2NF): **

- it is in 1NF and every non-primary key attribute is fully dependent on the primary
- all the incomplete dependencies have been removed.
- **No partial dependencies** (one or more of the attributes depends on only part of the primary key, occur when primary key is composite key)<fppmj12187c>

**3rd Normal Form (3NF):**

- it is in 1NF and 2NF and all non- key elements are fully dependent on the primary key. 
- **No non-key dependencies** <fppmj12187c>
  - non-key dependency: value of attribute is determined by another value (this is not part of the key)
- In other phrase: all attributes are dependent on the 
- No transitive dependencies (dependencies that are dependent on another attributes that are dependent on others, dependencies that are removable) <fppmj12187c>
- *MANY-TO-MANY functions cannot be directly normalized to 3NF, must use a 2 step process e.g.*

#### How to ensure a table is 3NF <fppmj13182c>

- No repeated attributes // data is atomic // No partial dependencies (no dual keys) 
- No non-key / transitive dependencies 



### 1.8.6 Data Definition Language (DDL)

#### DDL (Data Definition Language) 

- A syntax similar to a computer programming language for defining data structures, especially database schemas.

**SQL = Structured Query Language**

#### SQL Data Type

- Varchar
- INT
- Date
- [NOT FULLY INCLUDED]





#### SQL CREATE Database

```sql
CREATE DATBASE <database-name>
```



#### SQL CREATE Table

```sql
CREATE TABLE NAME(
UserName : Varchar(15) NOT NULL, (ONLY THE ID IS NOT NULL)
DataOfBirth : Date,
PRIMARY KEY (UserName)
);
```

***Only the id is not null*** <fppmj13182di>

#### SQL AlTER Table

```sql
ALTER TABLE <table-name>
ADD <field-name> <data-type>;

EXAMPLE
ALTER TABLE PLAYER
ADD DateOfBirth Date;
```



#### SQL ADD Primary Key

```sql
PRIMARY KEY (field)
```



#### SQL ADD Foreign key

```sql
FOREIGN KEY (field) REFERENCES <table>(field)
```



#### Example

```sql
CREATE DATABASE ‘Personnel.gdb’ 
CREATE TABLE Training(
	EmpID      INT NOT NULL,
  CourseTitle VARCHAR(30) NOT NULL,
  CourseDate  Date NOT NULL,
  PRIMARY KEY (EmpID, CourseDate)
 );
  
 FOREIGN KEY (EmpID) REFERENCES Employee(EmpID))
```



#### SQL SELECT 

```sql
SELECT <field-name>, <field-name>
FROM <table name>
WHERE <condition>;

SELECT NurseID, FamilyName
FROM B-NURSE
WHERE Specialism = 'THEATRE';

SELECT STUDENT.FirstName, STUDENT.LastName, STUDENT- QUALIFICATION.QualCode
FROM STUDENT, STUDENT-QUALIFICATION
WHERE STUDENT-QUALIFICATION.Grade = 'A'
AND STUDENT.StudentID = STUDENT-QUALIFICATION.StudentID;

SELECT STUDENT.LastName
FROM STUDENT, CLASS-GROUP
WHERE ClassID = "CS1" // WHERE (ClassID = "CS1")
AND CLASS-GROUP.StudentID = STUDENT.StudentID;
```



### 1.8.7 Data Manipulation Language (DML)



- Query and maintenance of data done using this language
  – written in SQL



#### CREATE Query

```sql
SELECT <field-name> 
FROM <table-name>
WHERE <search-condition>
ORDER BY <field-name>


GROUP BY <field-name> - used to ensure <field-nam> is not repeated
```

#### SQL INNERJOIN

```sql
SELECT <field name>
FROM <table1 name>
INNER JOIN <table2 name>
ON table1.<field name> = table2.<field name>;

```



### Data maintenance

#### SQL UPDATE 

```sql
UPDATE <table-name>
SET <condition>
WHERE <condition>;
                
UPDATE B-NURSE
SET FamilyName = 'Chi'
WHERE NurseID = '076';

```

#### SQL INSERT 

```sql
INSERT INTO <table-name>
(<field-name>, <field-name>)
VALUES (<val1>, <val2>);

```

#### SQL INSERT 

```sql
ALTER TABLE NAME(SHOP-SUPPLIER)
ADD Country : Varchar(25)

```

#### SQL DELETE

```sql
DELETE FROM <table-name>
WHERE <condition>

```





### P.S

Nibble means 4 bits