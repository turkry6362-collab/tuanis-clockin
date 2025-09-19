<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
    <title>Tuanis Clock In</title>
    <meta name="description" content="Sistema de registro con GPS - Tuanis Cleaning Services" />
    <style>
        * { box-sizing: border-box; font-family: 'Segoe UI', sans-serif; }
        body {
            background: linear-gradient(135deg, #1a2d6c, #4b2e83, #7c2d98, #b32e7a);
            color: white;
            padding: 20px;
            text-align: center;
            max-width: 600px;
            margin: auto;
            min-height: 100vh;
        }
        .overlay {
            background: rgba(0, 0, 0, 0.3);
            backdrop-filter: blur(5px);
            border-radius: 16px;
            padding: 25px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.4);
            width: 100%;
            max-width: 600px;
            margin: 20px auto;
        }
        h1 { 
            color: #fff; 
            margin: 10px 0; 
            font-size: 1.8em; 
            text-shadow: 0 1px 3px rgba(0,0,0,0.5);
        }
        .subtitle {
            color: #f0f0f0;
            font-weight: bold;
            margin: 5px 0 20px;
            font-size: 1.1em;
            text-shadow: 0 1px 2px rgba(0,0,0,0.5);
        }
        .lang-btn {
            position: absolute;
            top: 15px;
            right: 15px;
            background: #1a2d6c;
            color: white;
            border: none;
            padding: 10px 16px;
            border-radius: 24px;
            cursor: pointer;
            font-size: 1em;
            font-weight: bold;
            box-shadow: 0 4px 12px rgba(0,0,0,0.3);
            transition: all 0.3s ease;
            z-index: 100;
        }
        .lang-btn:hover {
            background: #30459a;
            transform: scale(1.08);
        }
        .lang-btn.active {
            background: #7c2d98;
            box-shadow: 0 0 0 3px white, 0 0 10px rgba(255,255,255,0.5);
        }

        .input-group {
            margin: 15px 0;
            text-align: left;
        }
        input, select {
            width: 100%;
            padding: 14px;
            margin: 5px 0;
            border: 1px solid #4a5568;
            border-radius: 8px;
            font-size: 1em;
            background: rgba(255,255,255,0.1);
            color: white;
            outline: none;
        }
        input:focus, select:focus {
            border-color: #7c2d98;
            background: rgba(255,255,255,0.2);
            box-shadow: 0 0 0 2px rgba(124, 45, 152, 0.3);
        }
        select option { color: black; }

        .distance-info {
            font-size: 0.9em;
            color: #ccc;
            margin-top: 6px;
            height: 20px;
        }

        .status {
            margin: 15px 0;
            font-weight: bold;
            color: #f0f0f0;
            min-height: 24px;
            text-shadow: 0 1px 2px rgba(0,0,0,0.5);
        }
        .authorized {
            color: #4CAF50;
        }

        button {
            background: #7c2d98;
            color: white;
            border: none;
            padding: 14px 24px;
            margin: 10px 5px;
            border-radius: 8px;
            font-size: 16px;
            cursor: pointer;
            min-width: 150px;
            transition: all 0.3s ease;
            box-shadow: 0 4px 10px rgba(124, 45, 152, 0.3);
        }
        button:disabled {
            background: #5a2d75;
            opacity: 0.7;
            cursor: not-allowed;
        }
        button:hover:not(:disabled) {
            background: #9c38c5;
            transform: translateY(-1px);
        }

        .message {
            padding: 12px;
            margin: 15px 0;
            border-radius: 8px;
            display: none;
            font-weight: bold;
            text-align: center;
        }
        .success { 
            background: rgba(46, 193, 80, 0.2); 
            color: #4CAF50; 
            border: 1px solid rgba(46, 193, 80, 0.4);
        }
        .error { 
            background: rgba(232, 55, 55, 0.2); 
            color: #F44336; 
            border: 1px solid rgba(232, 55, 55, 0.4);
        }

        .instructions {
            margin: 20px 0;
            text-align: left;
            font-size: 0.9em;
            color: #ddd;
            line-height: 1.5;
        }
        .time {
            font-size: 0.9em;
            color: #ccc;
            margin: 10px 0;
        }

        .admin-section {
            margin-top: 20px;
            padding: 15px;
            background: rgba(255,255,255,0.05);
            border-radius: 8px;
            display: none;
        }
        .admin-section input {
            background: rgba(255,255,255,0.15);
        }

        .photo-preview {
            margin: 15px 0;
            max-width: 100%;
            max-height: 200px;
            display: none;
            border-radius: 8px;
            border: 2px dashed rgba(255,255,255,0.3);
        }

        .actions {
            display: flex;
            justify-content: center;
            gap: 10px;
            flex-wrap: wrap;
        }

        #exportBtn {
            background: #2d7898;
        }
        #exportBtn:hover:not(:disabled) {
            background: #3a9ac5;
        }

        #resetBtn {
            background: #982d2d;
        }
        #resetBtn:hover:not(:disabled) {
            background: #c53a3a;
        }
    </style>
</head>
<body lang="es">
    <button id="languageToggle" class="lang-btn">EN</button>

    <div class="overlay">
        <h1 id="title">Registro de Asistencia</h1>
        <p class="subtitle">TUANIS CLEANING SERVICES</p>

        <div class="input-group">
            <label id="nameLabel" for="employeeName">Nombre Completo / Full Name</label>
            <input type="text" id="employeeName" inputmode="text" placeholder="Juan Pérez" />
        </div>

        <div class="input-group">
            <label id="idLabel" for="employeeId">ID de Empleado / Employee ID</label>
            <input type="text" id="employeeId" inputmode="numeric" placeholder="EMP001" />
        </div>

        <div class="input-group">
            <label id="locationLabel" for="locationSelect">Ubicación de Trabajo / Work Location</label>
            <select id="locationSelect">
                <option value="" disabled selected>-- Seleccione una ubicación / Select a location --</option>
            </select>
            <div class="distance-info" id="distanceInfo" aria-live="polite"></div>
        </div>

        <div class="status" id="locationStatus" aria-live="polite">Verificando ubicación... / Checking location...</div>
        <div class="time" id="currentTime">--:--:--</div>

        <div class="actions">
            <button id="clockInBtn" disabled>REGISTRAR ENTRADA / CLOCK IN</button>
            <button id="clockOutBtn" disabled>REGISTRAR SALIDA / CLOCK OUT</button>
            <button id="resetBtn" style="display:none;">LIMPIAR / CLEAR</button>
        </div>

        <button id="exportBtn">EXPORTAR REGISTROS / EXPORT LOGS</button>

        <div class="admin-section" id="adminSection">
            <h3 id="adminTitle">🔐 Modo Administrador</h3>
            <input type="password" id="adminPin" placeholder="PIN de administrador" maxlength="4" />
            <button id="overrideBtn">REGISTRAR FUERA DE RANGO</button>
        </div>

        <div class="photo-preview" id="photoPreview"></div>

        <div class="message success" id="successMessage" aria-live="assertive"></div>
        <div class="message error" id="errorMessage" aria-live="assertive"></div>

        <div class="instructions">
            <strong>Instrucciones / Instructions</strong><br>
            1. Ingrese su nombre e ID / Enter your name and ID<br>
            2. Seleccione una ubicación del menú / Select a location from dropdown<br>
            3. Verifique que esté dentro del rango permitido (1500m) / Verify you are within allowed range (1500m)<br>
            4. Toque el botón de entrada al comenzar / Tap clock in when starting<br>
            5. Toque el botón de salida al terminar / Tap clock out when ending<br>
            <br>
            <button id="toggleAdmin" style="background:#2d3a4d; font-size:0.8em; padding:6px 12px;">Modo Admin / Admin Mode</button>
        </div>
    </div>

    <script>
        // 🌐 Traducciones completas por idioma
        const translations = {
            es: {
                title: "Registro de Asistencia",
                subtitle: "TUANIS CLEANING SERVICES",
                nameLabel: "Nombre Completo / Full Name",
                idLabel: "ID de Empleado / Employee ID",
                locationLabel: "Ubicación de Trabajo / Work Location",
                clockInText: "REGISTRAR ENTRADA / CLOCK IN",
                clockOutText: "REGISTRAR SALIDA / CLOCK OUT",
                statusOutside: "Fuera del rango",
                statusInside: "Dentro del rango - listo para registrar",
                errorNoLocation: "Seleccione una ubicación",
                errorInvalidId: "ID debe comenzar con EMP",
                errorNoName: "Ingrese nombre completo",
                smsSent: "Notificación enviada al administrador",
                errorClockIn: "No se puede registrar: verifique ubicación, nombre e ID",
                instructionsTitle: "Instrucciones",
                language: "EN",
                placeholderName: "Juan Pérez",
                placeholderId: "EMP001",
                selectPlaceholder: "-- Seleccione una ubicación / Select a location --",
                overrideSuccess: "✅ Registro forzado por administrador",
                adminMode: "Modo Administrador",
                adminPinPlaceholder: "PIN de administrador",
                overrideBtn: "REGISTRAR FUERA DE RANGO",
                resetBtn: "LIMPIAR / CLEAR",
                exportBtn: "EXPORTAR REGISTROS / EXPORT LOGS",
                toggleAdmin: "Modo Admin / Admin Mode",
                photoLabel: "Foto tomada:",
                sessionRestored: "Sesión restaurada",
                csvFilename: "registros_tuanis.csv"
            },
            en: {
                title: "Attendance Check-In",
                subtitle: "TUANIS CLEANING SERVICES",
                nameLabel: "Full Name / Nombre Completo",
                idLabel: "Employee ID / ID de Empleado",
                locationLabel: "Work Location / Ubicación de Trabajo",
                clockInText: "CLOCK IN / REGISTRAR ENTRADA",
                clockOutText: "CLOCK OUT / REGISTRAR SALIDA",
                statusOutside: "Outside range",
                statusInside: "Inside range - ready to clock",
                errorNoLocation: "Select a location",
                errorInvalidId: "ID must start with EMP",
                errorNoName: "Enter full name",
                smsSent: "Notification sent to admin",
                errorClockIn: "Cannot clock in: check location, name and ID",
                instructionsTitle: "Instructions",
                language: "ES",
                placeholderName: "John Doe",
                placeholderId: "EMP001",
                selectPlaceholder: "-- Select a location / Seleccione una ubicación --",
                overrideSuccess: "✅ Override registered by admin",
                adminMode: "Admin Mode",
                adminPinPlaceholder: "Admin PIN",
                overrideBtn: "CLOCK IN ANYWAY",
                resetBtn: "CLEAR / LIMPIAR",
                exportBtn: "EXPORT LOGS / EXPORTAR REGISTROS",
                toggleAdmin: "Admin Mode / Modo Admin",
                photoLabel: "Photo captured:",
                sessionRestored: "Session restored",
                csvFilename: "tuanis_logs.csv"
            }
        };

        let currentLang = 'es';
        let logs = JSON.parse(localStorage.getItem('tuanisLogs')) || [];

        // Lista de ubicaciones
        const authorizedLocations = [
            { name: "1190 South Church Street, Mount Laurel, NJ 08054", lat: 39.9386, lng: -74.9097, radius: 1.5 },
            { name: "100 Lambert Way, Freehold, NJ 07728", lat: 40.2302, lng: -74.2736, radius: 1.5 },
            { name: "7600 Stenton Ave, Philadelphia, PA 19118", lat: 40.0708, lng: -75.1847, radius: 1.5 },
            { name: "1086 W King Rd, Malvern, PA 19355", lat: 40.0383, lng: -75.5367, radius: 1.5 },
            { name: "7715 Mc Calum St, Philadelphia, PA 19118", lat: 40.0678, lng: -75.1822, radius: 1.5 },
            { name: "375 North Dr, North Plainfield, NJ 07060", lat: 40.6158, lng: -74.4322, radius: 1.5 },
            { name: "10 Van Ness Court, Maplewood, NJ 07040", lat: 40.7314, lng: -74.4286, radius: 1.5 },
            { name: "2329 S Bonsall St, Philadelphia, PA 19145", lat: 39.9247, lng: -75.1792, radius: 1.5 }
        ];

        let userLocation = null;
        let selectedLocation = null;
        let isClockedIn = false;
        let lastClockInTime = null;

        // Elementos
        const languageToggle = document.getElementById("languageToggle");
        const titleEl = document.getElementById("title");
        const nameLabel = document.getElementById("nameLabel");
        const idLabel = document.getElementById("idLabel");
        const locationLabel = document.getElementById("locationLabel");
        const locationSelect = document.getElementById("locationSelect");
        const distanceInfo = document.getElementById("distanceInfo");
        const locationStatus = document.getElementById("locationStatus");
        const clockInBtn = document.getElementById("clockInBtn");
        const clockOutBtn = document.getElementById("clockOutBtn");
        const successMessage = document.getElementById("successMessage");
        const errorMessage = document.getElementById("errorMessage");
        const employeeNameInput = document.getElementById("employeeName");
        const employeeIdInput = document.getElementById("employeeId");
        const currentTimeEl = document.getElementById("currentTime");
        const resetBtn = document.getElementById("resetBtn");
        const exportBtn = document.getElementById("exportBtn");
        const adminSection = document.getElementById("adminSection");
        const adminPin = document.getElementById("adminPin");
        const overrideBtn = document.getElementById("overrideBtn");
        const toggleAdmin = document.getElementById("toggleAdmin");
        const adminTitle = document.getElementById("adminTitle");
        const photoPreview = document.getElementById("photoPreview");

        // PIN de administrador (en producción, esto debería validarse en backend)
        const ADMIN_PIN = "1234";

        // Cambiar idioma
        function toggleLanguage() {
            currentLang = currentLang === 'es' ? 'en' : 'es';
            
            document.documentElement.setAttribute('lang', currentLang);
            document.body.setAttribute('lang', currentLang);

            languageToggle.classList.add('active');
            setTimeout(() => languageToggle.classList.remove('active'), 300);

            updateTexts();
            populateDropdown();
            updateUI();
        }
        languageToggle.addEventListener('click', toggleLanguage);

        // Actualizar todos los textos según idioma
        function updateTexts() {
            const t = translations[currentLang];
            languageToggle.textContent = t.language;
            titleEl.textContent = t.title;
            nameLabel.textContent = t.nameLabel;
            idLabel.textContent = t.idLabel;
            locationLabel.textContent = t.locationLabel;
            clockInBtn.textContent = t.clockInText;
            clockOutBtn.textContent = t.clockOutText;
            adminTitle.textContent = `🔐 ${t.adminMode}`;
            adminPin.placeholder = t.adminPinPlaceholder;
            overrideBtn.textContent = t.overrideBtn;
            resetBtn.textContent = t.resetBtn;
            exportBtn.textContent = t.exportBtn;
            toggleAdmin.textContent = t.toggleAdmin;
            document.querySelector('.instructions strong').textContent = t.instructionsTitle + ' / ' + t.instructionsTitle;

            employeeNameInput.placeholder = t.placeholderName;
            employeeIdInput.placeholder = t.placeholderId;
        }

        // Llenar dropdown con traducción dinámica
        function populateDropdown() {
            const t = translations[currentLang];
            locationSelect.innerHTML = `<option value="" disabled selected>${t.selectPlaceholder}</option>`;
            authorizedLocations.forEach(loc => {
                const option = document.createElement("option");
                option.value = loc.name;
                option.textContent = loc.name;
                locationSelect.appendChild(option);
            });
        }

        // Cálculo de distancia
        function calculateDistance(lat1, lon1, lat2, lon2) {
            const R = 6371;
            const dLat = deg2rad(lat2 - lat1);
            const dLon = deg2rad(lon2 - lon1);
            const a =
                Math.sin(dLat/2) * Math.sin(dLat/2) +
                Math.cos(deg2rad(lat1)) * Math.cos(deg2rad(lat2)) *
                Math.sin(dLon/2) * Math.sin(dLon/2);
            const c = 2 * Math.atan2(Math.sqrt(a), Math.sqrt(1-a));
            return R * c; // km
        }
        function deg2rad(deg) { return deg * (Math.PI/180); }

        // Validar ID (EMP + números)
        function validateEmployeeId(id) {
            return /^EMP\d+$/.test(id.trim());
        }

        // Simular captura de foto (en móvil real, usaría getUserMedia)
        function simulatePhotoCapture() {
            const canvas = document.createElement('canvas');
            canvas.width = 320;
            canvas.height = 240;
            const ctx = canvas.getContext('2d');
            ctx.fillStyle = '#333';
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            ctx.fillStyle = '#fff';
            ctx.font = '20px Arial';
            ctx.fillText('📸 Photo Simulada', 40, 120);
            ctx.fillText(new Date().toLocaleString(), 40, 160);
            photoPreview.src = canvas.toDataURL();
            photoPreview.style.display = 'block';
            return canvas.toDataURL();
        }

        // Guardar en localStorage
        function saveSession() {
            const session = {
                name: employeeNameInput.value.trim(),
                id: employeeIdInput.value.trim(),
                lastLocation: selectedLocation?.name || ''
            };
            localStorage.setItem('tuanisSession', JSON.stringify(session));
        }

        // Restaurar sesión
        function restoreSession() {
            const session = JSON.parse(localStorage.getItem('tuanisSession'));
            if (session) {
                employeeNameInput.value = session.name;
                employeeIdInput.value = session.id;
                if (session.lastLocation) {
                    const option = Array.from(locationSelect.options).find(opt => opt.value === session.lastLocation);
                    if (option) {
                        locationSelect.value = session.lastLocation;
                        selectedLocation = authorizedLocations.find(loc => loc.name === session.lastLocation);
                    }
                }
                showMessage(translations[currentLang].sessionRestored, 'success');
            }
        }

        // Actualizar interfaz
        function updateUI() {
            const t = translations[currentLang];

            if (selectedLocation && userLocation) {
                const distance = calculateDistance(
                    userLocation.coords.latitude,
                    userLocation.coords.longitude,
                    selectedLocation.lat,
                    selectedLocation.lng
                );
                const meters = distance * 1000;
                
                // Crear enlace a Google Maps
                const mapLink = `https://www.google.com/maps/dir/${userLocation.coords.latitude},${userLocation.coords.longitude}/${selectedLocation.lat},${selectedLocation.lng}`;
                distanceInfo.innerHTML = `Distancia: ${meters.toFixed(0)} m <a href="${mapLink}" target="_blank" style="color:#7c2d98; text-decoration:underline;">(Ver ruta)</a>`;

                const statusText = distance <= selectedLocation.radius
                    ? t.statusInside
                    : t.statusOutside;
                locationStatus.textContent = `${statusText} (${distance.toFixed(2)} km)`;
                locationStatus.className = distance <= selectedLocation.radius ? "status authorized" : "status";
            } else {
                distanceInfo.textContent = "";
                locationStatus.textContent = selectedLocation ? "Obteniendo ubicación..." : "Seleccione una ubicación";
                locationStatus.className = "status";
            }

            // Validar campos
            const name = employeeNameInput.value.trim();
            const id = employeeIdInput.value.trim();
            const isIdValid = validateEmployeeId(id);
            const isNameValid = name.length > 0;

            if (!isNameValid && name.length > 0) {
                showMessage(t.errorNoName, 'error');
            }
            if (!isIdValid && id.length > 0) {
                showMessage(t.errorInvalidId, 'error');
            }

            const distance = selectedLocation && userLocation
                ? calculateDistance(
                    userLocation.coords.latitude,
                    userLocation.coords.longitude,
                    selectedLocation.lat,
                    selectedLocation.lng
                )
                : Infinity;

            const ready = isNameValid && isIdValid && selectedLocation && userLocation && distance <= selectedLocation.radius;

            clockInBtn.disabled = isClockedIn || !ready;
            clockOutBtn.disabled = !isClockedIn;
            resetBtn.style.display = isClockedIn ? 'none' : 'inline-block';
        }

        // Evento de selección
        locationSelect.addEventListener("change", () => {
            const selectedName = locationSelect.value;
            selectedLocation = authorizedLocations.find(loc => loc.name === selectedName) || null;
            updateUI();
        });

        // Mostrar mensaje
        function showMessage(text, type) {
            const el = type === 'success' ? successMessage : errorMessage;
            el.textContent = text;
            el.style.display = "block";
            setTimeout(() => el.style.display = "none", 3000);
        }

        // Simular SMS
        function sendSMS(message) {
            console.log(`SMS simulado al 914-291-8000: ${message}`);
            showMessage(translations[currentLang].smsSent, 'success');
        }

        // Registrar log
        function addLog(action, name, id, location, time, photo = null, override = false) {
            const log = { action, name, id, location, time, photo, override };
            logs.push(log);
            localStorage.setItem('tuanisLogs', JSON.stringify(logs));
        }

        // Clock In
        function clockIn(override = false) {
            const name = employeeNameInput.value.trim();
            const id = employeeIdInput.value.trim();
            if (!name) {
                showMessage(translations[currentLang].errorNoName, 'error');
                return;
            }
            if (!validateEmployeeId(id)) {
                showMessage(translations[currentLang].errorInvalidId, 'error');
                return;
            }
            if (!selectedLocation) {
                showMessage(translations[currentLang].errorNoLocation, 'error');
                return;
            }
            if (!userLocation && !override) {
                showMessage("Error de ubicación / Location error", 'error');
                return;
            }

            let distance = Infinity;
            if (userLocation) {
                distance = calculateDistance(
                    userLocation.coords.latitude,
                    userLocation.coords.longitude,
                    selectedLocation.lat,
                    selectedLocation.lng
                );
            }

            if (distance > selectedLocation.radius && !override) {
                showMessage(translations[currentLang].errorClockIn, 'error');
                return;
            }

            isClockedIn = true;
            lastClockInTime = new Date();
            const time = lastClockInTime.toLocaleString();
            const photo = simulatePhotoCapture(); // Simula foto

            const message = `${override ? '[ADMIN OVERRIDE] ' : ''}Entrada de ${name} (${id}) en ${selectedLocation.name} a las ${time}`;
            sendSMS(message);
            addLog('clock-in', name, id, selectedLocation.name, time, photo, override);
            saveSession();

            showMessage(`✅ Entrada registrada: ${time}`, 'success');
            updateUI();
        }
        clockInBtn.addEventListener('click', () => clockIn(false));

        // Clock Out
        function clockOut() {
            const name = employeeNameInput.value.trim();
            const id = employeeIdInput.value.trim();
            const clockOutTime = new Date();
            const diffMs = clockOutTime - lastClockInTime;
            const diffHours = (diffMs / (1000 * 60 * 60)).toFixed(2);

            const photo = simulatePhotoCapture(); // Simula foto al salir
            const time = clockOutTime.toLocaleString();

            sendSMS(`Salida de ${name} (${id}) de ${selectedLocation.name} a las ${time}. Horas trabajadas: ${diffHours}`);
            addLog('clock-out', name, id, selectedLocation.name, time, photo);

            isClockedIn = false;
            lastClockInTime = null;
            updateUI();
            showMessage(`👋 Salida registrada: ${time} | Horas: ${diffHours}`, 'success');
        }
        clockOutBtn.addEventListener('click', clockOut);

        // Reset Form
        function resetForm() {
            employeeNameInput.value = '';
            employeeIdInput.value = '';
            locationSelect.selectedIndex = 0;
            selectedLocation = null;
            photoPreview.style.display = 'none';
            photoPreview.src = '';
            updateUI();
        }
        resetBtn.addEventListener('click', resetForm);

        // Exportar CSV
        function exportCSV() {
            if (logs.length === 0) {
                showMessage("No hay registros para exportar", 'error');
                return;
            }

            const t = translations[currentLang];
            let csv = "Acción,Nombre,ID,Ubicación,Fecha,Hora,Foto,Override\n";
            logs.forEach(log => {
                const date = new Date(log.time);
                const dateString = date.toLocaleDateString();
                const timeString = date.toLocaleTimeString();
                csv += `"${log.action}","${log.name}","${log.id}","${log.location}","${dateString}","${timeString}","${log.photo ? 'Sí' : 'No'}","${log.override ? 'Sí' : 'No'}"\n`;
            });

            const blob = new Blob([csv], { type: 'text/csv;charset=utf-8;' });
            const link = document.createElement("a");
            const url = URL.createObjectURL(blob);
            link.setAttribute("href", url);
            link.setAttribute("download", t.csvFilename);
            link.style.visibility = 'hidden';
            document.body.appendChild(link);
            link.click();
            document.body.removeChild(link);
        }
        exportBtn.addEventListener('click', exportCSV);

        // Toggle Admin Mode
        toggleAdmin.addEventListener('click', () => {
            adminSection.style.display = adminSection.style.display === 'none' ? 'block' : 'none';
        });

        // Override Clock In
        overrideBtn.addEventListener('click', () => {
            if (adminPin.value === ADMIN_PIN) {
                clockIn(true);
                adminPin.value = '';
                adminSection.style.display = 'none';
                showMessage(translations[currentLang].overrideSuccess, 'success');
            } else {
                showMessage("PIN incorrecto", 'error');
            }
        });

        // Reloj en tiempo real
        setInterval(() => {
            currentTimeEl.textContent = new Date().toLocaleTimeString();
        }, 1000);

        // Obtener ubicación
        if (navigator.geolocation) {
            navigator.geolocation.watchPosition(
                (position) => {
                    userLocation = position;
                    updateUI();
                },
                (error) => {
                    locationStatus.textContent = "Error de ubicación / Location error";
                },
                { enableHighAccuracy: true, maximumAge: 30000, timeout: 10000 }
            );
        } else {
            locationStatus.textContent = "GPS no soportado / GPS not supported";
        }

        // Inicializar
        updateTexts();
        populateDropdown();
        restoreSession(); // ¡Carga la última sesión!
        updateUI();
    </script>
</body>
</html>
