# GWFluxHeunC
gravitational-wave energy flux

# GW Flux Calculator - User Guide

## 🪟 Windows Guide

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

## 🐧 Linux Guide

### 1. Install MATLAB Runtime R2025a
1. Extract `MATLAB_Runtime_R2025a_glnxa64.zip`.
2. Open terminal in the extracted folder and run:
   ```bash
   sudo ./install -destinationFolder /usr/local/MATLAB/MATLAB_Runtime/R2025a -mode silent -agreeToLicense yes
   ```
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
Default install path: `~/MATLAB/Apps/GW_Flux_Calculator`

### 3. Run Application
1. Navigate to the install directory:
   ```bash
   cd ~/MATLAB/Apps/GW_Flux_Calculator
   ```
2. Run the executable:
   ```bash
   ./GW_Flux_Calculator
   ```
3. The terminal will prompt:
   ```text
   Please enter the spin parameter a (|a| < 1): 
   ```
   Type your value (e.g., `0.5`) and press Enter.

### 4. Output Files
- The program automatically generates: `GWFlux_Report_a=0.X.txt`
- **Location:** Typically `/root/MathWorks/MatlabRuntimeCache/R2025a/` or the current working directory (if writable).
- **Content:** Same as Windows version.

---

## 🔧 Troubleshooting

| Platform | Issue | Solution |
|:---|:---|:---|
| **Windows** | `"MATLAB Runtime not found"` | Verify R2025a installed correctly. Restart PC. Re-run installer → select **Repair**. |
| **Linux** | `"libmwmclmcrrt.so: cannot open shared object file"` | Environment variables missing. Run the `export LD_LIBRARY_PATH=...` command from Section 1. |
| **Linux** | `Permission denied` | Run `chmod +x GW_Flux_Calculator` before execution. |
| **Both** | `"Invalid parameter a"` | Ensure `|a| < 1`. The Kerr black hole condition requires `a` strictly less than 1. |

---
**Version:** 1.0 | **MATLAB Runtime:** R2025a | **Support:** ckchen@mail.bnu.edu.cn
