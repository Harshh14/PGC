Sequential Matrix Multiplication
1. Open Windows PowerShell
2. Verify that WSL is installed
          (wsl --status)
3. List installed WSL distributions
           (wsl -l -v)
4. Start Ubuntu from PowerShell
           (wsl)
5. Update Ubuntu package information
          (sudo apt update)
6. Install GCC and build tools
   sudo apt install build-essential -y
7. Verify GCC
   (gcc --version)
8. Create the sequential experiment directory
     (mkdir -p ~/parallel_lab/sequential
     cd ~/parallel_lab/sequential)
9. Create the source file
     (nano matrix_sequential.c)
10. Compile the sequential program
(gcc -O2 matrix_sequential.c -o matrix_sequential)
11. Verify the executable
            ( ls -l )
12. Run the sequential program
      (./matrix_sequential)
