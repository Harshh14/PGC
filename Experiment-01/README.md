Part A - Sequential Matrix Multiplication
1. Open Windows PowerShell
2. Verify that WSL is installed (wsl --status)
<img width="1919" height="119" alt="1" src="https://github.com/user-attachments/assets/259dca3a-4008-427d-aefc-0d7027316ee0" />
3. List installed WSL distributions (wsl -l -v)
4. Start Ubuntu from PowerShell (wsl)
5. <img width="1919" height="129" alt="2" src="https://github.com/user-attachments/assets/8ef9b17a-df4e-4b0b-8bb0-2abe9dcadddd" />
6. Update Ubuntu package information (sudo apt update)
7. <img width="1919" height="481" alt="3 1" src="https://github.com/user-attachments/assets/7fbf6907-4f54-4405-9fe9-b2918939cc1b" />
8. Install GCC and build tools ( sudo apt install build-essential -y)
9. <img width="1919" height="930" alt="3 2" src="https://github.com/user-attachments/assets/203c37a4-ab25-4b4a-9a2e-eaa474a29624" />
10. Verify GCC (gcc --version)
11. <img width="1919" height="85" alt="4" src="https://github.com/user-attachments/assets/178b1359-c7db-4bf3-a7e8-58e5aa6f8516" />
12. Create the sequential experiment directory ( mkdir -p ~/parallel_lab/sequential
cd ~/parallel_lab/sequential)
<img width="1919" height="63" alt="5" src="https://github.com/user-attachments/assets/29ebd76f-1fa4-4c16-ae85-71d3b474fc9b" />
14. Create the source file (nano matrix_sequential.c)
15. Compile the sequential program ( gcc -O2 matrix_sequential.c -o matrix_sequential)
16. Verify the executable (ls -l)
18. Run the sequential program (./matrix_sequential)
19. <img width="1919" height="30" alt="6" src="https://github.com/user-attachments/assets/77685d36-d939-4a8b-a500-ac24aef99368" />
20. Sequential Result 
Sequential Matrix Multiplication Completed
Matrix Size = 4000 x 4000
Execution Time = 244.120000 seconds
Verification C[0][0] = 4000.00
)
(Initializing 4000 x 4000 matrices...<img width="1919" height="142" alt="8" src="https://github.com/user-attachments/assets/6aed3fc3-c47e-425d-ba58-3f2a86c6f57c" />
 

