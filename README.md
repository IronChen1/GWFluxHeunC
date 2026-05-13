# How to cite
```text
@article{Chen:2026bym,
    author = "Chen, Changkai and Cao, Zhoujian and Jing, Jiliang",
    title = "{Efficient and Stable Computation of Gravitational-Wave Fluxes from Generic Kerr Orbits via a Unified HeunC Framework}",
    eprint = "2605.09250",
    archivePrefix = "arXiv",
    primaryClass = "gr-qc",
    month = "5",
    year = "2026"}
 ```
# 📥 Download & Installation Guide

> **⚠️ Important Note for Downloading:**
> The software package is provided as **split archives** (multi-part zip files).
> - **Direct Download:** You must download **all** parts (`.z01`, `.z02`, ..., `.zip`) and place them in the **same folder** before extracting.
> - **BitTorrent:** If you have trouble downloading the files directly, please use the provided `.torrent` file.
> - **Support:** If you still encounter difficulties, please email me at **ckchen@mail.bnu.edu.cn**.

# GW Flux Calculator - User Guide

##  Windows Guide

### 1. Install MATLAB Runtime R2025a
1. Extract `MATLAB_Runtime_R2025a_win64.zip`.
2. Run `setup.exe`.
3. Accept the license agreement and follow the wizard.
4. Default path: `C:\Program Files\MATLAB\MATLAB Runtime\R2025a`.
5. Wait 5–10 minutes, then **restart your computer**.

### 2. Install Application
1. Double-click `GW_Flux_Calculator.exe` (the installer).
2. Follow the installation wizard.
3. Default install folder: `C:\Program Files\GW_Flux_Calculator`.

### 3. Run Application
1. Open the installation folder.
2. **Double-click `GW_Flux_Calculator.exe`**.
3. A **parameter input window** will pop up automatically.
4. Enter the black hole spin parameter `a` (must satisfy `|a| < 1`, e.g., `0.5`) and click **OK**.

### 4. Output Files
- The program automatically generates a report: `GWFlux_Report_a=0.X.txt`
- **Location:** Usually saved in the application folder or `C:\Users\<YourName>\Documents\MATLAB\`.
- **Content:** Parameter config, total energy flux summary, and detailed mode components (16 significant digits).

---

# GW Flux Calculator - User Guide

## 🐧 Linux Guide

### 1. Install MATLAB Runtime R2025a
1. Extract `MATLAB_Runtime_R2025a_glnxa64.zip`.
2. Open terminal in the extracted folder and run:
   ```bash
   sudo ./install
   ```
   Follow the installation wizard (accept license, choose default path).

3. **Configure Environment Variables** (Critical):
   ```bash
   echo 'export LD_LIBRARY_PATH=/usr/local/MATLAB/MATLAB_Runtime/R2025a/runtime/glnxa64:/usr/local/MATLAB/MATLAB_Runtime/R2025a/bin/glnxa64:/usr/local/MATLAB/MATLAB_Runtime/R2025a/sys/os/glnxa64:$LD_LIBRARY_PATH' >> ~/.bashrc
   source ~/.bashrc
   ```

4. **Install System Dependencies** (Ubuntu/Debian):
   ```bash
   sudo apt install -y libx11-6 libxrender1 libxtst6 libstdc++6 libgomp1
   ```

### 2. Install Application
```bash
chmod +x GW_Flux_Calculator.install
./GW_Flux_Calculator.install
```
Default install path: `~/GW_Flux_Calculator`

### 3. Run Application

**Method 1: Using the Run Script (Recommended)**

1. Navigate to your installation directory:
   ```bash
   cd ~/GW_Flux_Calculator/application/
   ```
   *(Note: This is an example path. Your actual path depends on where you installed the application.)*

2. Run the executable script:
   ```bash
   ./run_GW_Flux_Calculator.sh /usr/local/MATLAB/MATLAB_Runtime/R2025a
   ```
   *(Note: `/usr/local/MATLAB/MATLAB_Runtime/R2025a` is the example Runtime path. Replace it with your actual MATLAB Runtime installation path if different.)*

3. The terminal will prompt:
   ```text
   Please enter the spin parameter a (|a| < 1): 
   ```
   Type your value (e.g., `0.5`) and press Enter.

**Method 2: Direct Execution (If Environment Variables are Set)**

If you've configured `LD_LIBRARY_PATH` correctly (Step 1.3), you can also run:
```bash
cd ~/GW_Flux_Calculator/application/
./GW_Flux_Calculator
```
Then enter parameter `a` when prompted.

### 4. Output Files
- The program automatically generates: `GWFlux_Report_a=0.X.txt`
- **Location:** Typically `/root/MathWorks/MatlabRuntimeCache/R2025a/` or the current working directory (if writable).
- **Content:** Same as Windows version.

---
**Version:** 1.0 | **MATLAB Runtime:** R2025a | **Support:** ckchen@mail.bnu.edu.cn
