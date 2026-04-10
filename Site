<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>☕ Coffee Redação</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #1a1a2e 0%, #16213e 50%, #0f3460 100%);
            min-height: 100vh;
            color: #fff;
        }
        
        .hidden { display: none !important; }
        
        /* Login Screen */
        .login-screen {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 20px;
        }
        
        .login-container {
            background: rgba(255,255,255,0.05);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255,255,255,0.1);
            border-radius: 20px;
            padding: 40px;
            width: 100%;
            max-width: 400px;
            text-align: center;
        }
        
        .coffee-icon {
            font-size: 64px;
            margin-bottom: 15px;
            animation: bounce 2s infinite;
        }
        
        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }
        
        .login-container h1 {
            font-size: 28px;
            margin-bottom: 8px;
            background: linear-gradient(135deg, #d4a574, #6f4e37);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        .login-container p {
            color: #b8b8d1;
            font-size: 14px;
            margin-bottom: 30px;
        }
        
        .input-group {
            margin-bottom: 20px;
            text-align: left;
        }
        
        .input-group label {
            display: block;
            font-size: 12px;
            color: #b8b8d1;
            margin-bottom: 6px;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }
        
        .input-group input {
            width: 100%;
            background: rgba(255,255,255,0.05);
            border: 1px solid rgba(255,255,255,0.1);
            border-radius: 12px;
            padding: 14px 16px;
            color: #fff;
            font-size: 15px;
            transition: all 0.3s;
        }
        
        .input-group input:focus {
            outline: none;
            border-color: #6f4e37;
            box-shadow: 0 0 0 3px rgba(111,78,55,0.2);
        }
        
        .login-btn {
            width: 100%;
            background: linear-gradient(135deg, #6f4e37, #4a3428);
            border: none;
            border-radius: 12px;
            padding: 16px;
            color: #fff;
            font-size: 16px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
            margin-top: 10px;
        }
        
        .login-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 20px rgba(111,78,55,0.3);
        }
        
        .login-btn:disabled {
            opacity: 0.6;
            cursor: not-allowed;
            transform: none;
        }
        
        .error-msg {
            background: rgba(244,67,54,0.1);
            border: 1px solid rgba(244,67,54,0.3);
            border-radius: 8px;
            padding: 12px;
            color: #f44336;
            font-size: 13px;
            margin-top: 15px;
            display: none;
        }
        
        .error-msg.show { display: block; }
        
        /* Dashboard */
        .dashboard {
            min-height: 100vh;
        }
        
        .header {
            background: rgba(255,255,255,0.03);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid rgba(255,255,255,0.05);
            padding: 15px 30px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
            font-weight: 700;
            font-size: 20px;
        }
        
        .logo span:first-child {
            font-size: 28px;
        }
        
        .user-info {
            display: flex;
            align-items: center;
            gap: 12px;
        }
        
        .user-avatar {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: linear-gradient(135deg, #6f4e37, #4a3428);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 18px;
        }
        
        .user-details {
            text-align: left;
        }
        
        .user-name {
            font-weight: 600;
            font-size: 14px;
        }
        
        .user-class {
            font-size: 12px;
            color: #7a7a9d;
        }
        
        .header-actions {
            display: flex;
            gap: 10px;
        }
        
        .icon-btn {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: rgba(255,255,255,0.05);
            border: 1px solid rgba(255,255,255,0.1);
            color: #b8b8d1;
            cursor: pointer;
            transition: all 0.3s;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .icon-btn:hover {
            background: rgba(255,255,255,0.1);
            color: #fff;
        }
        
        /* Summary Cards */
        .summary {
            padding: 30px;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
        }
        
        .summary-card {
            background: rgba(255,255,255,0.03);
            border: 1px solid rgba(255,255,255,0.05);
            border-radius: 16px;
            padding: 20px;
            display: flex;
            align-items: center;
            gap: 15px;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .summary-card:hover {
            transform: translateY(-3px);
            background: rgba(255,255,255,0.05);
        }
        
        .summary-card.tasks { border-left: 3px solid #2196f3; }
        .summary-card.essays { border-left: 3px solid #d4a574; }
        .summary-card.warnings { border-left: 3px solid #ff9800; }
        .summary-card.achievements { border-left: 3px solid #4caf50; }
        
        .card-icon {
            width: 50px;
            height: 50px;
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
        }
        
        .tasks .card-icon { background: rgba(33,150,243,0.1); }
        .essays .card-icon { background: rgba(212,165,116,0.1); }
        .warnings .card-icon { background: rgba(255,152,0,0.1); }
        .achievements .card-icon { background: rgba(76,175,80,0.1); }
        
        .card-info h3 {
            font-size: 28px;
            font-weight: 700;
        }
        
        .card-info p {
            font-size: 12px;
            color: #7a7a9d;
            text-transform: uppercase;
        }
        
        /* Tabs */
        .tabs {
            display: flex;
            gap: 5px;
            padding: 0 30px;
            border-bottom: 1px solid rgba(255,255,255,0.05);
        }
        
        .tab-btn {
            background: none;
            border: none;
            padding: 15px 25px;
            color: #7a7a9d;
            font-size: 14px;
            font-weight: 500;
            cursor: pointer;
            transition: all 0.3s;
            position: relative;
            border-radius: 12px 12px 0 0;
        }
        
        .tab-btn:hover {
            color: #b8b8d1;
            background: rgba(255,255,255,0.03);
        }
        
        .tab-btn.active {
            color: #d4a574;
            background: rgba(212,165,116,0.05);
        }
        
        .tab-btn.active::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            height: 3px;
            background: #d4a574;
            border-radius: 3px 3px 0 0;
        }
        
        /* Content */
        .content {
            padding: 30px;
        }
        
        .tab-panel {
            display: none;
            animation: fadeIn 0.3s;
        }
        
        .tab-panel.active {
            display: block;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .panel-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 25px;
        }
        
        .panel-header h2 {
            font-size: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        select {
            background: rgba(255,255,255,0.05);
            border: 1px solid rgba(255,255,255,0.1);
            border-radius: 8px;
            padding: 8px 15px;
            color: #fff;
            cursor: pointer;
        }
        
        /* Items List */
        .items-list {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }
        
        .item-card {
            background: rgba(255,255,255,0.03);
            border: 1px solid rgba(255,255,255,0.05);
            border-radius: 16px;
            padding: 20px;
            transition: all 0.3s;
            cursor: pointer;
        }
        
        .item-card:hover {
            background: rgba(255,255,255,0.05);
            transform: translateX(5px);
        }
        
        .item-header {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            margin-bottom: 10px;
        }
        
        .item-title {
            font-size: 16px;
            font-weight: 600;
            flex: 1;
            margin-right: 15px;
        }
        
        .badge {
            padding: 4px 12px;
            border-radius: 20px;
            font-size: 11px;
            font-weight: 500;
            text-transform: uppercase;
        }
        
        .badge-pending { background: rgba(255,152,0,0.15); color: #ff9800; }
        .badge-completed { background: rgba(76,175,80,0.15); color: #4caf50; }
        .badge-overdue { background: rgba(244,67,54,0.15); color: #f44336; }
        .badge-essay { background: rgba(212,165,116,0.15); color: #d4a574; }
        
        .item-meta {
            display: flex;
            gap: 20px;
            font-size: 13px;
            color: #7a7a9d;
            margin-bottom: 10px;
        }
        
        .item-description {
            font-size: 14px;
            color: #b8b8d1;
            line-height: 1.5;
        }
        
        .item-footer {
            margin-top: 15px;
            padding-top: 15px;
            border-top: 1px solid rgba(255,255,255,0.05);
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .item-subject {
            font-size: 12px;
            color: #7a7a9d;
        }
        
        .item-action {
            background: linear-gradient(135deg, #6f4e37, #4a3428);
            border: none;
            border-radius: 8px;
            padding: 8px 16px;
            color: #fff;
            font-size: 13px;
            font-weight: 500;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .item-action:hover {
            transform: scale(1.05);
            box-shadow: 0 5px 15px rgba(111,78,55,0.3);
        }
        
        .empty-state {
            text-align: center;
            padding: 60px 20px;
            color: #7a7a9d;
        }
        
        .empty-state i {
            font-size: 48px;
            margin-bottom: 15px;
            opacity: 0.5;
        }
        
        .loading {
            text-align: center;
            padding: 40px;
            color: #d4a574;
        }
        
        .loading::after {
            content: '';
            display: inline-block;
            width: 20px;
            height: 20px;
            border: 2px solid #d4a574;
            border-top-color: transparent;
            border-radius: 50%;
            margin-left: 10px;
            animation: spin 1s linear infinite;
        }
        
        @keyframes spin {
            to { transform: rotate(360deg); }
        }
        
        /* Toast */
        .toast-container {
            position: fixed;
            top: 20px;
            right: 20px;
            z-index: 1000;
            display: flex;
            flex-direction: column;
            gap: 10px;
        }
        
        .toast {
            background: rgba(255,255,255,0.1);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255,255,255,0.1);
            border-radius: 12px;
            padding: 15px 20px;
            display: flex;
            align-items: center;
            gap: 12px;
            min-width: 300px;
            animation: slideIn 0.3s;
        }
        
        @keyframes slideIn {
            from { transform: translateX(100%); opacity: 0; }
            to { transform: translateX(0); opacity: 1; }
        }
        
        .toast.success { border-left: 3px solid #4caf50; }
        .toast.error { border-left: 3px solid #f44336; }
        .toast.info { border-left: 3px solid #2196f3; }
        
        /* Responsive */
        @media (max-width: 768px) {
            .header {
                padding: 15px 20px;
                flex-wrap: wrap;
                gap: 10px;
            }
            
            .summary {
                padding: 20px;
                grid-template-columns: repeat(2, 1fr);
            }
            
            .tabs {
                padding: 0 20px;
                overflow-x: auto;
            }
            
            .tab-btn {
                white-space: nowrap;
            }
            
            .content {
                padding: 20px;
            }
        }
    </style>
</head>
<body>
    <!-- Login Screen -->
    <div id="loginScreen" class="login-screen">
        <div class="login-container">
            <div class="coffee-icon">☕</div>
            <h1>Coffee Redação</h1>
            <p>Sua rotina escolar, mais organizada</p>
            
            <form id="loginForm">
                <div class="input-group">
                    <label>RA (Registro do Aluno)</label>
                    <input type="text" id="username" placeholder="000123456789-0" required>
                </div>
                
                <div class="input-group">
                    <label>Senha</label>
                    <input type="password" id="password" placeholder="Sua senha" required>
                </div>
                
                <button type="submit" class="login-btn" id="loginBtn">
                    Entrar
                </button>
            </form>
            
            <div id="errorMsg" class="error-msg"></div>
            
            <p style="margin-top: 20px; font-size: 12px; color: #7a7a9d;">
                Conectado às APIs oficiais da Sala do Futuro
            </p>
        </div>
    </div>

    <!-- Dashboard -->
    <div id="dashboard" class="dashboard hidden">
        <header class="header">
            <div class="logo">
                <span>☕</span>
                <span>Coffee Redação</span>
            </div>
            
            <div class="user-info">
                <div class="user-avatar">👤</div>
                <div class="user-details">
                    <div id="userName" class="user-name">Carregando...</div>
                    <div id="userClass" class="user-class">-</div>
                </div>
            </div>
            
            <div class="header-actions">
                <button class="icon-btn" onclick="refreshData()" title="Atualizar">🔄</button>
                <button class="icon-btn" onclick="logout()" title="Sair">🚪</button>
            </div>
        </header>

        <!-- Summary Cards -->
        <div class="summary">
            <div class="summary-card tasks" onclick="switchTab('tasks')">
                <div class="card-icon">📚</div>
                <div class="card-info">
                    <h3 id="taskCount">-</h3>
                    <p>Tarefas</p>
                </div>
            </div>
            
            <div class="summary-card essays" onclick="switchTab('essays')">
                <div class="card-icon">✍️</div>
                <div class="card-info">
                    <h3 id="essayCount">-</h3>
                    <p>Redações</p>
                </div>
            </div>
            
            <div class="summary-card warnings" onclick="switchTab('warnings')">
                <div class="card-icon">🔔</div>
                <div class="card-info">
                    <h3 id="warningCount">-</h3>
                    <p>Avisos</p>
                </div>
            </div>
            
            <div class="summary-card achievements" onclick="switchTab('grades')">
                <div class="card-icon">🏆</div>
                <div class="card-info">
                    <h3 id="achievementCount">-</h3>
                    <p>Conquistas</p>
                </div>
            </div>
        </div>

        <!-- Tabs -->
        <div class="tabs">
            <button class="tab-btn active" onclick="switchTab('tasks')">📚 Tarefas</button>
            <button class="tab-btn" onclick="switchTab('essays')">✍️ Redações</button>
            <button class="tab-btn" onclick="switchTab('warnings')">🔔 Avisos</button>
            <button class="tab-btn" onclick="switchTab('grades')">📊 Notas</button>
        </div>

        <!-- Content -->
        <div class="content">
            <!-- Tasks Tab -->
            <div id="tasksPanel" class="tab-panel active">
                <div class="panel-header">
                    <h2>📚 Tarefas Pendentes</h2>
                    <select id="taskFilter" onchange="filterTasks()">
                        <option value="all">Todas</option>
                        <option value="pending">Pendentes</option>
                        <option value="overdue">Atrasadas</option>
                    </select>
                </div>
                <div id="tasksList" class="items-list">
                    <div class="loading">Carregando...</div>
                </div>
            </div>

            <!-- Essays Tab -->
            <div id="essaysPanel" class="tab-panel">
                <div class="panel-header">
                    <h2>✍️ Redações</h2>
                    <select id="essayFilter" onchange="filterEssays()">
                        <option value="all">Todas</option>
                        <option value="pending">Pendentes</option>
                        <option value="submitted">Enviadas</option>
                    </select>
                </div>
                <div id="essaysList" class="items-list">
                    <div class="loading">Carregando...</div>
                </div>
            </div>

            <!-- Warnings Tab -->
            <div id="warningsPanel" class="tab-panel">
                <div class="panel-header">
                    <h2>🔔 Mural de Avisos</h2>
                </div>
                <div id="warningsList" class="items-list">
                    <div class="loading">Carregando...</div>
                </div>
            </div>

            <!-- Grades Tab -->
            <div id="gradesPanel" class="tab-panel">
                <div class="panel-header">
                    <h2>📊 Boletim</h2>
                </div>
                <div id="gradesList" class="items-list">
                    <div class="loading">Carregando...</div>
                </div>
            </div>
        </div>
    </div>

    <div id="toastContainer" class="toast-container"></div>

    <script>
        // ==========================================
        // CONFIGURAÇÃO DAS APIs
        // ==========================================
        const API_BASE = 'https://sedintegracoes.educacao.sp.gov.br/saladofuturobffapi';
        const EDUSP_API = 'https://edusp-api.ip.tv';
        
        // Estado
        let auth = {
            sedToken: null,
            eduspToken: null,
            user: null
        };
        
        let data = {
            tasks: [],
            essays: [],
            warnings: [],
            grades: [],
            achievements: []
        };

        // ==========================================
        // LOGIN
        // ==========================================
        document.getElementById('loginForm').addEventListener('submit', async (e) => {
            e.preventDefault();
            
            const username = document.getElementById('username').value;
            const password = document.getElementById('password').value;
            const btn = document.getElementById('loginBtn');
            const errorDiv = document.getElementById('errorMsg');
            
            btn.disabled = true;
            btn.textContent = 'Entrando...';
            errorDiv.classList.remove('show');
            
            try {
                // 1. Login no SED
                const loginRes = await fetch(`${API_BASE}/credenciais/api/LoginCompletoToken`, {
                    method: 'POST',
                    headers: { 'Content-Type': 'application/json' },
                    body: JSON.stringify({ username, password })
                });
                
                if (!loginRes.ok) throw new Error('Credenciais inválidas');
                
                const loginData = await loginRes.json();
                
                if (!loginData.token) throw new Error('Erro na autenticação');
                
                auth.sedToken = loginData.token;
                auth.user = loginData.usuario;
                
                // 2. Obter token EDUSP
                const eduspRes = await fetch(`${EDUSP_API}/registration/edusp/token`, {
                    method: 'POST',
                    headers: { 'Content-Type': 'application/json' },
                    body: JSON.stringify({ sedToken: auth.sedToken })
                });
                
                if (eduspRes.ok) {
                    const eduspData = await eduspRes.json();
                    auth.eduspToken = eduspData.token;
                }
                
                // Salvar no localStorage
                localStorage.setItem('coffeeAuth', JSON.stringify(auth));
                
                showToast('success', 'Login realizado com sucesso!');
                showDashboard();
                loadAllData();
                
            } catch (error) {
                console.error('Erro no login:', error);
                errorDiv.textContent = error.message || 'Erro ao fazer login. Tente novamente.';
                errorDiv.classList.add('show');
            } finally {
                btn.disabled = false;
                btn.textContent = 'Entrar';
            }
        });

        // ==========================================
        // FUNÇÕES AUXILIARES
        // ==========================================
        function showDashboard() {
            document.getElementById('loginScreen').classList.add('hidden');
            document.getElementById('dashboard').classList.remove('hidden');
            
            if (auth.user) {
                document.getElementById('userName').textContent = auth.user.nome || 'Aluno';
                document.getElementById('userClass').textContent = auth.user.turma || 'Turma não definida';
            }
        }

        function logout() {
            localStorage.removeItem('coffeeAuth');
            auth = { sedToken: null, eduspToken: null, user: null };
            document.getElementById('dashboard').classList.add('hidden');
            document.getElementById('loginScreen').classList.remove('hidden');
            document.getElementById('loginForm').reset();
            showToast('info', 'Você saiu do sistema');
        }

        function switchTab(tab) {
            // Atualizar botões
            document.querySelectorAll('.tab-btn').forEach(btn => btn.classList.remove('active'));
            event.target.classList.add('active');
            
            // Atualizar painéis
            document.querySelectorAll('.tab-panel').forEach(panel => panel.classList.remove('active'));
            document.getElementById(tab + 'Panel').classList.add('active');
        }

        function showToast(type, message) {
            const container = document.getElementById('toastContainer');
            const toast = document.createElement('div');
            toast.className = `toast ${type}`;
            
            const icons = { success: '✓', error: '✕', info: 'ℹ' };
            toast.innerHTML = `<span style="font-size: 20px;">${icons[type]}</span><span>${message}</span>`;
            
            container.appendChild(toast);
            setTimeout(() => toast.remove(), 4000);
        }

        // ==========================================
        // CARREGAMENTO DE DADOS
        // ==========================================
        async function loadAllData() {
            await Promise.all([
                loadTasks(),
                loadEssays(),
                loadWarnings(),
                loadGrades(),
                loadAchievements()
            ]);
            updateSummary();
        }

        async function apiCall(endpoint, options = {}) {
            const url = endpoint.startsWith('http') ? endpoint : `${API_BASE}${endpoint}`;
            const config = {
                headers: {
                    'Authorization': `Bearer ${auth.sedToken}`,
                    'Content-Type': 'application/json',
                    ...options.headers
                },
                ...options
            };
            
            try {
                const res = await fetch(url, config);
                if (!res.ok) throw new Error(`HTTP ${res.status}`);
                return await res.json();
            } catch (error) {
                console.error('API Error:', error);
                throw error;
            }
        }

        async function loadTasks() {
            try {
                // Buscar tarefas do TMS (Task Management System)
                const result = await apiCall(`${EDUSP_API}/tms/task/todo?limit=100&offset=0`, {
                    headers: { 'Authorization': `Bearer ${auth.eduspToken || auth.sedToken}` }
                });
                
                data.tasks = result.tasks || result.data || [];
                renderTasks();
            } catch (e) {
                console.error('Erro ao carregar tarefas:', e);
                document.getElementById('tasksList').innerHTML = `
                    <div class="empty-state">
                        <div style="font-size: 48px; margin-bottom: 15px;">📭</div>
                        <p>Não foi possível carregar as tarefas</p>
                        <p style="font-size: 12px; margin-top: 10px;">Verifique sua conexão ou tente novamente</p>
                    </div>
                `;
            }
        }

        async function loadEssays() {
            try {
                // Buscar redações (is_essay=true)
                const result = await apiCall(`${EDUSP_API}/tms/task/todo?is_essay=true&with_answer=true&limit=100`, {
                    headers: { 'Authorization': `Bearer ${auth.eduspToken || auth.sedToken}` }
                });
                
                data.essays = result.tasks || result.data || [];
                renderEssays();
            } catch (e) {
                console.error('Erro ao carregar redações:', e);
                document.getElementById('essaysList').innerHTML = `
                    <div class="empty-state">
                        <div style="font-size: 48px; margin-bottom: 15px;">✍️</div>
                        <p>Nenhuma redação encontrada</p>
                    </div>
                `;
            }
        }

        async function loadWarnings() {
            try {
                if (!auth.user?.codigo) return;
                
                const result = await apiCall(`/muralavisosapi/api/mural-avisos/listar-avisos-turma?CodigoUsuario=${auth.user.codigo}&PerfilAviso=1`);
                
                data.warnings = result.avisos || result.data || [];
                renderWarnings();
            } catch (e) {
                console.error('Erro ao carregar avisos:', e);
                data.warnings = [];
                renderWarnings();
            }
        }

        async function loadGrades() {
            try {
                if (!auth.user?.codigo) return;
                
                const result = await apiCall(`/apiboletim/api/Avaliacao/GetAvaliacaoAluno?codigoAluno=${auth.user.codigo}`);
                
                data.grades = result.avaliacoes || result.data || [];
                renderGrades();
            } catch (e) {
                console.error('Erro ao carregar notas:', e);
                data.grades = [];
                renderGrades();
            }
        }

        async function loadAchievements() {
            try {
                const result = await apiCall(`${EDUSP_API}/achievement/user/achievement?goal_period=week`, {
                    headers: { 'Authorization': `Bearer ${auth.eduspToken || auth.sedToken}` }
                });
                
                data.achievements = result.achievements || result.data || [];
                document.getElementById('achievementCount').textContent = data.achievements.length;
            } catch (e) {
                document.getElementById('achievementCount').textContent = '0';
            }
        }

        function updateSummary() {
            const pendingTasks = data.tasks.filter(t => !t.completed).length;
            const pendingEssays = data.essays.filter(e => !e.answer_submitted).length;
            
            document.getElementById('taskCount').textContent = pendingTasks;
            document.getElementById('essayCount').textContent = pendingEssays;
            document.getElementById('warningCount').textContent = data.warnings.length;
        }

        // ==========================================
        // RENDERIZAÇÃO
        // ==========================================
        function renderTasks() {
            const container = document.getElementById('tasksList');
            
            if (data.tasks.length === 0) {
                container.innerHTML = `
                    <div class="empty-state">
                        <div style="font-size: 48px; margin-bottom: 15px;">🎉</div>
                        <p>Nenhuma tarefa pendente!</p>
                        <p style="font-size: 12px; margin-top: 10px;">Aproveite para revisar o conteúdo</p>
                    </div>
                `;
                return;
            }
            
            container.innerHTML = data.tasks.map(task => `
                <div class="item-card" onclick="openItem('${task.id}', 'task')">
                    <div class="item-header">
                        <div class="item-title">${task.title || 'Tarefa'}</div>
                        <span class="badge ${task.completed ? 'badge-completed' : 'badge-pending'}">
                            ${task.completed ? 'Concluída' : 'Pendente'}
                        </span>
                    </div>
                    <div class="item-meta">
                        <span>📅 ${task.due_date ? new Date(task.due_date).toLocaleDateString('pt-BR') : 'Sem prazo'}</span>
                        <span>⏱️ ${task.estimated_time || '-'} min</span>
                    </div>
                    ${task.description ? `<div class="item-description">${task.description.substring(0, 100)}...</div>` : ''}
                    <div class="item-footer">
                        <span class="item-subject">📚 ${task.subject || 'Geral'}</span>
                        <button class="item-action">Acessar</button>
                    </div>
                </div>
            `).join('');
        }

        function renderEssays() {
            const container = document.getElementById('essaysList');
            
            if (data.essays.length === 0) {
                container.innerHTML = `
                    <div class="empty-state">
                        <div style="font-size: 48px; margin-bottom: 15px;">✨</div>
                        <p>Nenhuma redação pendente!</p>
                    </div>
                `;
                return;
            }
            
            container.innerHTML = data.essays.map(essay => `
                <div class="item-card" onclick="openItem('${essay.id}', 'essay')">
                    <div class="item-header">
                        <div class="item-title">${essay.title || 'Redação'}</div>
                        <span class="badge ${essay.answer_submitted ? 'badge-completed' : 'badge-essay'}">
                            ${essay.answer_submitted ? 'Enviada' : 'Pendente'}
                        </span>
                    </div>
                    <div class="item-meta">
                        <span>📅 ${essay.due_date ? new Date(essay.due_date).toLocaleDateString('pt-BR') : 'Sem prazo'}</span>
                        <span>📝 ${essay.word_count || '800-1000'} palavras</span>
                    </div>
                    ${essay.theme ? `<div class="item-description"><strong>Tema:</strong> ${essay.theme}</div>` : ''}
                    <div class="item-footer">
                        <span class="item-subject">✍️ Redação</span>
                        <button class="item-action">${essay.answer_submitted ? 'Ver' : 'Escrever'}</button>
                    </div>
                </div>
            `).join('');
        }

        function renderWarnings() {
            const container = document.getElementById('warningsList');
            
            if (data.warnings.length === 0) {
                container.innerHTML = `
                    <div class="empty-state">
                        <div style="font-size: 48px; margin-bottom: 15px;">🔕</div>
                        <p>Nenhum aviso no momento</p>
                    </div>
                `;
                return;
            }
            
            container.innerHTML = data.warnings.map(warning => `
                <div class="item-card">
                    <div class="item-header">
                        <div class="item-title">${warning.titulo || 'Aviso'}</div>
                        <span class="badge badge-pending">Novo</span>
                    </div>
                    <div class="item-meta">
                        <span>📅 ${warning.data ? new Date(warning.data).toLocaleDateString('pt-BR') : '-'}</span>
                        <span>👤 ${warning.autor || 'Professor'}</span>
                    </div>
                    <div class="item-description">${warning.mensagem || warning.conteudo || ''}</div>
                </div>
            `).join('');
        }

        function renderGrades() {
            const container = document.getElementById('gradesList');
            
            if (data.grades.length === 0) {
                container.innerHTML = `
                    <div class="empty-state">
                        <div style="font-size: 48px; margin-bottom: 15px;">📊</div>
                        <p>Notas não disponíveis</p>
                        <p style="font-size: 12px; margin-top: 10px;">As notas aparecerão quando forem lançadas</p>
                    </div>
                `;
                return;
            }
            
            container.innerHTML = data.grades.map(grade => `
                <div class="item-card">
                    <div class="item-header">
                        <div class="item-title">${grade.disciplina || 'Disciplina'}</div>
                        <span class="badge ${grade.nota >= 6 ? 'badge-completed' : grade.nota >= 4 ? 'badge-pending' : 'badge-overdue'}">
                            ${grade.nota !== undefined ? grade.nota.toFixed(1) : '-'}
                        </span>
                    </div>
                    <div class="item-meta">
                        <span>📚 ${grade.bimestre || 'Bimestre atual'}</span>
                        <span>📝 ${grade.avaliacao || 'Avaliação'}</span>
                    </div>
                    ${grade.observacao ? `<div class="item-description">${grade.observacao}</div>` : ''}
                </div>
            `).join('');
        }

        // ==========================================
        // FILTROS
        // ==========================================
        function filterTasks() {
            const filter = document.getElementById('taskFilter').value;
            let filtered = data.tasks;
            
            if (filter === 'pending') filtered = data.tasks.filter(t => !t.completed);
            else if (filter === 'overdue') {
                filtered = data.tasks.filter(t => {
                    const due = t.due_date ? new Date(t.due_date) : null;
                    return due && due < new Date() && !t.completed;
                });
            }
            
            const container = document.getElementById('tasksList');
            if (filtered.length === 0) {
                container.innerHTML = `
                    <div class="empty-state">
                        <p>Nenhuma tarefa encontrada com este filtro</p>
                    </div>
                `;
            } else {
                container.innerHTML = filtered.map(task => `
                    <div class="item-card" onclick="openItem('${task.id}', 'task')">
                        <div class="item-header">
                            <div class="item-title">${task.title || 'Tarefa'}</div>
                            <span class="badge ${task.completed ? 'badge-completed' : 'badge-pending'}">
                                ${task.completed ? 'Concluída' : 'Pendente'}
                            </span>
                        </div>
                        <div class="item-meta">
                            <span>📅 ${task.due_date ? new Date(task.due_date).toLocaleDateString('pt-BR') : 'Sem prazo'}</span>
                        </div>
                        <div class="item-footer">
                            <span class="item-subject">📚 ${task.subject || 'Geral'}</span>
                            <button class="item-action">Acessar</button>
                        </div>
                    </div>
                `).join('');
            }
        }

        function filterEssays() {
            const filter = document.getElementById('essayFilter').value;
            let filtered = data.essays;
            
            if (filter === 'pending') filtered = data.essays.filter(e => !e.answer_submitted);
            else if (filter === 'submitted') filtered = data.essays.filter(e => e.answer_submitted);
            
            const container = document.getElementById('essaysList');
            if (filtered.length === 0) {
                container.innerHTML = `
                    <div class="empty-state">
                        <p>Nenhuma redação encontrada com este filtro</p>
                    </div>
                `;
            } else {
                container.innerHTML = filtered.map(essay => `
                    <div class="item-card" onclick="openItem('${essay.id}', 'essay')">
                        <div class="item-header">
                            <div class="item-title">${essay.title || 'Redação'}</div>
                            <span class="badge ${essay.answer_submitted ? 'badge-completed' : 'badge-essay'}">
                                ${essay.answer_submitted ? 'Enviada' : 'Pendente'}
                            </span>
                        </div>
                        <div class="item-footer">
                            <span class="item-subject">✍️ Redação</span>
                            <button class="item-action">${essay.answer_submitted ? 'Ver' : 'Escrever'}</button>
                        </div>
                    </div>
                `).join('');
            }
        }

        function openItem(id, type) {
            const url = type === 'essay' 
                ? `https://saladofuturo.educacao.sp.gov.br/redacao/${id}`
                : `https://saladofuturo.educacao.sp.gov.br/tarefa/${id}`;
            window.open(url, '_blank');
        }

        function refreshData() {
            showToast('info', 'Atualizando dados...');
            loadAllData();
        }

        // ==========================================
        // INICIALIZAÇÃO
        // ==========================================
        window.onload = () => {
            const saved = localStorage.getItem('coffeeAuth');
            if (saved) {
                try {
                    auth = JSON.parse(saved);
                    if (auth.sedToken) {
                        showDashboard();
                        loadAllData();
                    }
                } catch (e) {
                    console.error('Erro ao restaurar sessão:', e);
                }
            }
        };
    </script>
</body>
</html>
