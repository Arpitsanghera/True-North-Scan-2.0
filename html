<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>True North Scan 🇨🇦</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.1.1/css/all.min.css">
    <script src="https://cdn.jsdelivr.net/npm/quagga@0.12.1/dist/quagga.min.js"></script>
    <style>
        body {
            font-family: 'Inter', sans-serif;
            transition: background-color 0.3s ease, color 0.3s ease;
        }
        .hidden-file-input {
            display: none;
        }
        body.dark {
            background-color: #121212;
            color: #e0e0e0;
        }
        .dark #app-container {
            background-color: #1e1e1e;
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.4), 0 10px 10px -5px rgba(0, 0, 0, 0.3);
        }
        .dark .text-primary { color: #b71c1c; }
        .dark .text-gray-600 { color: #b0b0b0; }
        .dark .text-indigo-700 { color: #a0a8e0; }
        .dark .text-gray-500 { color: #8b8b8b; }
        .dark .text-gray-800 { color: #e0e0e0; }
        .dark .border-gray-200 { border-color: #333; }
        .dark .bg-gray-100 { background-color: #2d2d2d; }
        .dark .hover\:bg-gray-200:hover { background-color: #3a3a3a; }
        .allergen { color: #ff4500; font-weight: bold; }
        #scanner-container {
            margin: 1rem 0;
            position: relative;
            width: 100%;
            max-width: 400px;
            height: 300px;
            border: 3px solid #B22222; /* Canadian Red border */
            border-radius: 8px;
            overflow: hidden;
            margin-left: auto;
            margin-right: auto;
            display: none;
            cursor: crosshair;
        }
        #interactive.viewport {
            position: absolute; top: 0; left: 0; width: 100%; height: 100%;
        }
        #interactive video {
            width: 100%; height: 100%; object-fit: cover;
        }
        #scanner-overlay {
            position: absolute; top: 0; left: 0; width: 100%; height: 100%;
            display: flex; align-items: center; justify-content: center;
            pointer-events: none;
        }
        .scanner-frame {
            width: 80%; height: 50%; border: 2px solid #fff;
            box-shadow: 0 0 0 9999px rgba(0, 0, 0, 0.5);
            animation: pulse 1.5s infinite;
        }
        @keyframes pulse {
            0% { box-shadow: 0 0 0 9999px rgba(0, 0, 0, 0.5); }
            50% { box-shadow: 0 0 0 9999px rgba(0, 0, 0, 0.6); }
            100% { box-shadow: 0 0 0 9999px rgba(0, 0, 0, 0.5); }
        }
        #scanner-message {
            position: absolute; bottom: 20px; color: #fff; text-align: center;
            padding: 0.5rem 1rem; background-color: rgba(0, 0, 0, 0.5);
            border-radius: 0.5rem;
        }
        #progressBar {
            transition: width 0.4s ease-in-out;
        }
    </style>
</head>
<body class="min-h-screen bg-white p-4 sm:p-6 lg:p-8 flex items-center justify-center dark:bg-gray-900">
    <div id="app-container" class="bg-gray-50 dark:bg-gray-800 rounded-3xl shadow-2xl p-6 sm:p-8 lg:p-10 w-full max-w-lg transform transition-all duration-300 relative">
        <button id="themeToggle" class="absolute top-4 right-4 p-2 rounded-full bg-gray-200 dark:bg-gray-700 text-gray-800 dark:text-gray-200 focus:outline-none focus:ring-2 focus:ring-red-500" aria-label="Toggle dark mode">
            <i class="fas fa-moon hidden dark:block"></i>
            <i class="fas fa-sun dark:hidden"></i>
        </button>

        <h1 class="text-4xl font-extrabold text-center text-red-700 dark:text-red-500 mb-8 tracking-tight" tabindex="0">
            True North Scan 🇨🇦
        </h1>

        <p class="text-center text-gray-600 mb-8 text-lg leading-relaxed dark:text-gray-400" tabindex="0">
            Uncover the true Canadian story behind every product. Simply scan a barcode or use the search bar.
        </p>

        <div class="mb-6">
            <div class="relative">
                <input
                    type="text"
                    id="searchBar"
                    placeholder="Search for a product..."
                    class="w-full pl-12 pr-4 py-3 rounded-full bg-gray-100 dark:bg-gray-700 text-gray-800 dark:text-gray-200 focus:outline-none focus:ring-2 focus:ring-red-500"
                >
                <i class="fas fa-search absolute left-4 top-1/2 transform -translate-y-1/2 text-gray-500 dark:text-gray-400"></i>
                <i class="fa-solid fa-leaf absolute right-4 top-1/2 transform -translate-y-1/2 text-red-500 dark:text-red-400"></i>
            </div>
        </div>

        <div class="flex flex-col justify-center mb-8 space-y-4 sm:space-y-0 sm:space-x-4 sm:flex-row">
            <button
                id="scanButton"
                class="bg-red-700 text-white font-bold py-4 px-6 rounded-full shadow-md hover:bg-red-800 transition-colors duration-200 focus:outline-none focus:ring-4 focus:ring-red-300 flex items-center justify-center space-x-3"
                aria-label="Scan a product barcode using your camera"
            >
                <i class="fas fa-camera text-xl"></i>
                <span>Scan with Camera</span>
            </button>

            <button
                id="fileScanButton"
                class="bg-gray-200 text-gray-800 font-bold py-4 px-6 rounded-full shadow-md hover:bg-gray-300 transition-colors duration-200 focus:outline-none focus:ring-4 focus:ring-gray-400 flex items-center justify-center space-x-3 dark:bg-gray-700 dark:text-gray-200 dark:hover:bg-gray-600"
                aria-label="Upload an image file to scan a barcode"
            >
                <i class="fas fa-upload text-xl"></i>
                <span>Upload from File</span>
            </button>
            <input type="file" accept="image/*" id="fileInput" class="hidden-file-input" />
        </div>

        <div class="flex justify-center mb-8">
            <button
                id="historyButton"
                class="bg-gray-200 text-gray-800 font-bold py-4 px-6 rounded-full shadow-md hover:bg-gray-300 transition-colors duration-200 focus:outline-none focus:ring-4 focus:ring-gray-400 flex items-center space-x-3 dark:bg-gray-700 dark:text-gray-200 dark:hover:bg-gray-600"
                aria-label="View scan history"
            >
                <i class="fas fa-history text-xl"></i>
                <span>History</span>
            </button>
        </div>

        <div id="scanner-container">
          <video id="video" muted playsinline></video>
          <div id="scanner-overlay">
              <div class="scanner-frame"></div>
              <div id="scanner-message">Scanning...</div>
          </div>
          <button id="closeScannerButton" class="absolute top-4 left-4 p-2 rounded-full bg-red-500 text-white focus:outline-none focus:ring-2 focus:ring-red-400" style="display: none;" aria-label="Close scanner">
              <i class="fas fa-times"></i>
          </button>
        </div>

        <div id="progressContainer" class="hidden w-full bg-gray-200 rounded-full h-2.5 dark:bg-gray-700 mb-6">
            <div id="progressBar" class="bg-red-600 h-2.5 rounded-full" style="width: 0%"></div>
        </div>
        <div id="loadingIndicator" class="hidden text-center text-red-700 dark:text-red-300 text-xl font-semibold mb-6 flex flex-col items-center">
            <div class="animate-spin rounded-full h-12 w-12 border-b-4 border-red-500 mb-4"></div>
            <p id="loadingMessage">Analyzing with AI...</p>
        </div>

        <div id="errorMessage" class="hidden bg-red-100 border border-red-400 text-red-700 px-4 py-3 rounded-xl relative mb-6" role="alert" aria-live="assertive">
            <strong class="font-bold">Error!</strong>
            <span id="errorText" class="block sm:inline"></span>
        </div>

        <div id="productInfoDisplay" class="hidden bg-gray-100 dark:bg-gray-800 p-6 rounded-2xl shadow-inner border border-gray-200 dark:border-gray-700" role="region" aria-live="polite">
        </div>

        <div id="historyModal" class="hidden fixed inset-0 bg-gray-900 bg-opacity-75 z-50 flex items-center justify-center p-4" role="dialog" aria-modal="true" aria-labelledby="historyModalTitle">
            <div class="bg-white dark:bg-gray-800 rounded-3xl shadow-2xl p-6 w-full max-w-lg max-h-[80vh] overflow-y-auto transform transition-all duration-300">
                <div class="flex justify-between items-center mb-6">
                    <h2 id="historyModalTitle" class="text-2xl font-bold text-red-700 dark:text-red-500">Scan History</h2>
                    <button id="closeHistoryModal" class="text-gray-500 dark:text-gray-400 hover:text-gray-800 dark:hover:text-gray-200" aria-label="Close scan history">
                        <i class="fas fa-times text-xl"></i>
                    </button>
                </div>
                <div id="historyList">
                </div>
                <button id="clearHistory" class="mt-4 w-full bg-red-700 text-white font-bold py-2 px-4 rounded-full hover:bg-red-800 transition-colors duration-200">Clear History</button>
            </div>
        </div>

        <div class="mt-10 pt-6 border-t border-gray-200 dark:border-gray-700 text-center text-gray-500 dark:text-gray-400 text-xs">
            <p class="mb-2">
                <strong>Disclaimer:</strong> The information provided by True North Scan is for general informational purposes only. It is not intended as legal, financial, or professional advice. Users should conduct their own research and verify all information independently.
            </p>
            <p class="mb-2">
                <strong>Privacy Policy:</strong> Your privacy is important to us. No images or personal data are stored, transmitted, or shared. All barcode scanning is performed locally on your device. Only the numerical barcode is sent to our secure server to retrieve publicly available product information. We do not track your location or store your scan history outside of your device's local storage.
            </p>
            <p>&copy; 2025 True North Scan. All rights reserved.</p>
        </div>

    </div>
    
    <audio id="shutterSound" src="https://www.soundjay.com/buttons/sounds/button-7.mp3" preload="auto"></audio>

    <script type="module" src="frontend.js"></script>
</body>
</html>
