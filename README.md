# Compressible Flow Calculator

A modern web application for calculating isentropic flow properties of a perfect gas with γ = 1.27.

## Features

- **Interactive Calculator**: Input Mach number and instantly get flow properties
- **Real-time Calculations**: All computations performed client-side with JavaScript
- **Clean UI**: Modern, responsive design with smooth animations
- **Flow Properties Calculated**:
  - Temperature Ratio (T/Tt)
  - Pressure Ratio (p/pt)
  - Area Ratio (A/A*)
  - Mass Flow Parameter (MFP)

## Parameters

- **Specific Heat Ratio**: γ = 1.27
- **Valid Mach Range**: 0.0 ≤ M ≤ 10.0
- **Flow Type**: Isentropic

## Equations

The calculator uses the following isentropic flow relations:

1. **Temperature Ratio**:
   ```
   T/Tt = [1 + ((γ-1)/2) × M²]⁻¹
   ```

2. **Pressure Ratio**:
   ```
   p/pt = [1 + ((γ-1)/2) × M²]⁻γ/(γ-1)
   ```

3. **Area Ratio**:
   ```
   A/A* = (1/M) × {[2/(γ+1)] × [1 + ((γ-1)/2) × M²]}^((γ+1)/(2(γ-1)))
   ```

4. **Mass Flow Parameter**:
   ```
   MFP = M × [γ × {1 + ((γ-1)/2) × M²}⁻(γ+1)/(2(γ-1))]^(1/2)
   ```

## Deployment on Vercel

### Method 1: Deploy with Vercel CLI

1. Install Vercel CLI (if not already installed):
   ```bash
   npm install -g vercel
   ```

2. Navigate to the project directory:
   ```bash
   cd compressible-flow-calculator
   ```

3. Deploy:
   ```bash
   vercel
   ```

4. Follow the prompts to complete deployment

### Method 2: Deploy via GitHub

1. Create a new repository on GitHub

2. Push your files to the repository:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/yourusername/compressible-flow-calculator.git
   git push -u origin main
   ```

3. Go to [Vercel Dashboard](https://vercel.com/dashboard)

4. Click "Add New Project"

5. Import your GitHub repository

6. Vercel will automatically detect the configuration and deploy

### Method 3: Drag and Drop

1. Go to [Vercel Dashboard](https://vercel.com/dashboard)

2. Click "Add New Project"

3. Drag and drop the folder containing `index.html` and `vercel.json`

4. Click "Deploy"

## File Structure

```
compressible-flow-calculator/
├── index.html       # Main application file
├── vercel.json      # Vercel deployment configuration
└── README.md        # This file
```

## Usage

1. Open the application in your web browser
2. Enter a Mach number in the input field (between 0.0 and 10.0)
3. Click "Calculate Properties" or press Enter
4. View the calculated flow properties in the results panel

## Flow Regimes

- **Subsonic**: M < 1.0
- **Sonic**: M = 1.0 (throat condition)
- **Supersonic**: M > 1.0

## Technical Details

- **Technology**: Pure HTML/CSS/JavaScript (no frameworks)
- **Styling**: Modern, clean design with Inter font family
- **Responsive**: Works on desktop, tablet, and mobile devices
- **Browser Support**: All modern browsers (Chrome, Firefox, Safari, Edge)

## Notes

- At M = 0, the area ratio (A/A*) approaches infinity
- At M = 1.0, A/A* = 1.0 (by definition, this is the throat)
- The Mass Flow Parameter (MFP) reaches its maximum value around M ≈ 1.5 for γ = 1.27

## License

Free to use for educational and engineering purposes.

## Contact

For questions or suggestions, please open an issue on GitHub.
