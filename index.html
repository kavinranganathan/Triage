<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MRI Triage System</title>
    <style>
        :root {
            --primary: #6a11cb;
            --primary-light: #8d67d6;
            --background: #f4f6f9;
            --text-dark: #1a1a2e;
            --text-light: #f8f9fa;
            --border-radius: 12px;
            --shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--background);
            color: var(--text-dark);
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        .header {
            background-color: var(--primary);
            color: var(--text-light);
            padding: 20px;
            border-radius: var(--border-radius);
            margin-bottom: 20px;
            box-shadow: var(--shadow);
        }

        .header h1 {
            font-size: 24px;
            font-weight: 600;
        }

        .tabs {
            display: flex;
            background-color: white;
            border-radius: var(--border-radius);
            overflow: hidden;
            box-shadow: var(--shadow);
            margin-bottom: 20px;
        }

        .tab {
            flex: 1;
            padding: 15px;
            text-align: center;
            cursor: pointer;
            color: var(--primary);
            font-weight: 500;
            transition: all 0.3s ease;
            border-bottom: 3px solid transparent;
        }

        .tab:hover {
            background-color: rgba(106, 17, 203, 0.05);
        }

        .tab.active {
            border-bottom-color: var(--primary);
            background-color: rgba(106, 17, 203, 0.1);
        }

        .tab-content {
            display: none;
            background-color: white;
            border-radius: var(--border-radius);
            padding: 20px;
            box-shadow: var(--shadow);
        }

        .tab-content.active {
            display: block;
        }

        .upload-section {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        .file-input-wrapper {
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        .file-input {
            display: none;
        }

        .file-input-label {
            background-color: var(--primary);
            color: white;
            padding: 12px 20px;
            border-radius: var(--border-radius);
            cursor: pointer;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            transition: background-color 0.3s ease;
        }

        .file-input-label:hover {
            background-color: var(--primary-light);
        }

        .file-list {
            border: 2px dashed var(--primary);
            border-radius: var(--border-radius);
            padding: 15px;
            min-height: 100px;
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        .result-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .result-card {
            background-color: white;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow);
            overflow: hidden;
            transition: transform 0.3s ease;
        }

        .result-card:hover {
            transform: translateY(-5px);
        }

        .result-image {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }

        .result-details {
            padding: 15px;
        }

        .severity-badge {
            display: inline-block;
            padding: 5px 10px;
            border-radius: 20px;
            font-size: 12px;
            font-weight: 600;
            margin-bottom: 10px;
        }

        .severity-critical {
            background-color: #ff4d4d;
            color: white;
        }

        .severity-urgent {
            background-color: #ff8c1a;
            color: white;
        }

        .severity-moderate {
            background-color: #4d79ff;
            color: white;
        }

        .severity-low {
            background-color: #2ecc71;
            color: white;
        }

        .more-details {
            display: none;
            padding: 10px;
            background-color: #f9f9f9;
            border-top: 1px solid #eee;
        }

        .result-card.expanded .more-details {
            display: block;
        }

        .more-details-toggle {
            cursor: pointer;
            color: var(--primary);
            user-select: none;
            margin-top: 10px;
            text-align: right;
            font-size: 0.9em;
        }

        .radiologist-notes {
            width: 100%;
            min-height: 100px;
            margin-top: 10px;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: var(--border-radius);
        }

        .status-message {
            padding: 15px;
            border-radius: var(--border-radius);
            margin-bottom: 15px;
            text-align: center;
        }

        .status-success {
            background-color: rgba(46, 204, 113, 0.1);
            color: #2ecc71;
            border: 1px solid rgba(46, 204, 113, 0.2);
        }

        .status-info {
            background-color: rgba(52, 152, 219, 0.1);
            color: #3498db;
            border: 1px solid rgba(52, 152, 219, 0.2);
        }

        .spinner {
            display: flex;
            justify-content: center;
            align-items: center;
            margin: 20px 0;
        }

        .spinner::after {
            content: '';
            width: 50px;
            height: 50px;
            border: 5px solid var(--primary);
            border-top-color: transparent;
            border-radius: 50%;
            animation: spin 1s linear infinite;
        }

        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
    </style>
</head>
<body>
    <div class="container">
        <header class="header">
            <h1>MRI Triage System</h1>
        </header>

        <div class="tabs">
            <div class="tab active" data-tab="new-analysis">New Analysis</div>
            <div class="tab" data-tab="upload">Upload Image</div>
            <div class="tab" data-tab="history">History</div>
        </div>

        <div class="tab-content active" id="new-analysis-content">
            <button id="fetchImagesBtn" class="file-input-label">
                Fetch & Analyze Images
            </button>
            <div id="statusMessage"></div>
            <div id="results" class="result-grid"></div>
        </div>

        <div class="tab-content" id="upload-content">
            <div class="upload-section">
                <div class="file-input-wrapper">
                    <input type="file" id="fileInput" class="file-input" accept="image/*" multiple>
                    <label for="fileInput" class="file-input-label">
                        Select MRI Images
                    </label>
                    <div id="fileList" class="file-list">No files selected</div>
                </div>
                <div class="button-group">
                    <button id="uploadBtn" class="file-input-label">Upload & Analyze</button>
                    <button id="clearFilesBtn" class="file-input-label" style="background-color: #7f8c8d;">Clear Selection</button>
                </div>
            </div>
            <div id="uploadStatusMessage"></div>
            <div id="uploadResults" class="result-grid"></div>
        </div>

        <div class="tab-content" id="history-content">
            <div id="historyResults" class="result-grid"></div>
        </div>
    </div>

    <script>
        // Utility Functions
        function toggleLoading(show, elementId = 'statusMessage') {
            const statusMessage = document.getElementById(elementId);
            
            if (show) {
                statusMessage.innerHTML = `
                    <div class="spinner"></div>
                `;
            } else {
                statusMessage.innerHTML = '';
            }
        }

        function showStatusMessage(message, type = 'info', elementId = 'statusMessage') {
            const statusDiv = document.getElementById(elementId);
            statusDiv.innerHTML = `
                <div class="status-message status-${type}">
                    ${message}
                </div>
            `;
        }

        function getSeverityInfo(rating) {
            if (rating >= 9) return { class: 'severity-critical', label: 'Critical' };
            if (rating >= 7) return { class: 'severity-urgent', label: 'Urgent' };
            if (rating >= 4) return { class: 'severity-moderate', label: 'Moderate' };
            return { class: 'severity-low', label: 'Low' };
        }

        function truncateText(text, maxLength = 100) {
            if (!text) return 'No details available';
            if (text.length <= maxLength) return text;
            return text.substr(0, maxLength) + '...';
        }

        function createResultCard(result, isHistory = false) {
            const severityInfo = getSeverityInfo(result.severity_rating || 0);
            const truncatedComment = truncateText(result.comment, 150);
            
            return `
                <div class="result-card" data-image-name="${result.image_name || ''}">
                    <img src="data:image/jpeg;base64,${result.image_data}" class="result-image" alt="MRI Scan">
                    <div class="result-details">
                        <span class="severity-badge ${severityInfo.class}">
                            ${severityInfo.label}
                        </span>
                        <h3>${result.image_name || 'MRI Scan'}</h3>
                        <p><strong>Severity Rating:</strong> ${(result.severity_rating || 0).toFixed(1)}/10</p>
                        <p class="truncate-text" data-full-text="${result.comment || ''}">
                            ${truncatedComment}
                            ${result.comment && result.comment.length > 150 
                                ? '<span class="more-link">More</span>' 
                                : ''}
                        </p>
                        <div class="more-details-toggle">ⓘ More Details</div>
                        <div class="more-details">
                            <p><strong>Detailed Comment:</strong> ${result.comment || 'No additional details'}</p>
                            ${result.radiologist_notes 
                                ? `<p><strong>Radiologist Notes:</strong> ${result.radiologist_notes}</p>` 
                                : ''}
                        </div>
                        ${!isHistory 
                            ? `<textarea placeholder="Add radiologist notes..." class="radiologist-notes"></textarea>
                               <button class="save-notes-btn file-input-label" style="margin-top: 10px;">Save Notes</button>`
                            : ''}
                    </div>
                </div>
            `;
        }

        // Tab Switching
        document.querySelectorAll('.tab').forEach(tab => {
            tab.addEventListener('click', () => {
                document.querySelectorAll('.tab').forEach(t => t.classList.remove('active'));
                document.querySelectorAll('.tab-content').forEach(tc => tc.classList.remove('active'));
                
                tab.classList.add('active');
                document.getElementById(`${tab.dataset.tab}-content`).classList.add('active');

                // Fetch history when history tab is clicked
                if (tab.dataset.tab === 'history') {
                    fetchHistory();
                }
            });
        });

        // File upload handling
        document.getElementById('fileInput').addEventListener('change', function(e) {
            const fileList = document.getElementById('fileList');
            fileList.innerHTML = '';
            
            Array.from(this.files).forEach(file => {
                const fileItem = document.createElement('div');
                fileItem.textContent = file.name;
                fileList.appendChild(fileItem);
            });
        });

        document.getElementById('uploadBtn').addEventListener('click', () => {
            const fileInput = document.getElementById('fileInput');
            const uploadStatusMessage = document.getElementById('uploadStatusMessage');
            const uploadResults = document.getElementById('uploadResults');

            if (fileInput.files.length === 0) {
                uploadStatusMessage.innerHTML = '<div class="status-message status-info">Please select at least one image</div>';
                return;
            }

            const formData = new FormData();
            for (let file of fileInput.files) {
                formData.append('file', file);
            }

            toggleLoading(true, 'uploadStatusMessage');
            fetch('/upload-image', {
                method: 'POST',
                body: formData
            })
                .then(response => response.json())
                .then(data => {
                    toggleLoading(false, 'uploadStatusMessage');
                    uploadResults.innerHTML = ''; // Clear previous results
                    
                    if (data.results) {
                        data.results.forEach(result => {
                            uploadResults.innerHTML += createResultCard(result);
                        });
                        uploadStatusMessage.innerHTML = `<div class="status-message status-success">Successfully uploaded and analyzed ${data.results.length} image(s)</div>`;
                    } else if (data.error) {
                        uploadStatusMessage.innerHTML = `<div class="status-message status-info">${data.error}</div>`;
                    }
                })
                .catch(error => {
                    toggleLoading(false, 'uploadStatusMessage');
                    uploadStatusMessage.innerHTML = '<div class="status-message status-info">Upload failed. Please try again.</div>';
                    console.error('Error:', error);
                });
        });

        // Clear file selection
        document.getElementById('clearFilesBtn').addEventListener('click', () => {
            document.getElementById('fileInput').value = '';
            document.getElementById('fileList').innerHTML = 'No files selected';
            document.getElementById('uploadResults').innerHTML = '';
            document.getElementById('uploadStatusMessage').innerHTML = '';
        });

        // Fetch Images
        document.getElementById('fetchImagesBtn').addEventListener('click', () => {
            toggleLoading(true);
            fetch('/fetch-images', { method: 'POST' })
                .then(response => response.json())
                .then(data => {
                    toggleLoading(false);
                    const resultsContainer = document.getElementById('results');
                    resultsContainer.innerHTML = '';

                    if (data.processed_count === 0) {
                        showStatusMessage('No new images found for analysis.', 'info');
                        return;
                    }

                    data.results.forEach(result => {
                        resultsContainer.innerHTML += createResultCard(result);
                    });

                    showStatusMessage(`Successfully fetched ${data.processed_count} new MRI images.`, 'success');
                })
                .catch(error => {
                    toggleLoading(false);
                    showStatusMessage('Failed to fetch images. Please try again.', 'info');
                    console.error('Error:', error);
                });
        });

        // Event delegation for various interactions
        document.addEventListener('click', (e) => {
            // More details toggle
            if (e.target.classList.contains('more-details-toggle')) {
                const resultCard = e.target.closest('.result-card');
                resultCard.classList.toggle('expanded');
            }

            // More details popup
            if (e.target.classList.contains('more-link')) {
                const fullText = e.target.closest('.truncate-text').dataset.fullText;
                alert(fullText);
            }

            // Save notes
            if (e.target.classList.contains('save-notes-btn')) {
                const resultCard = e.target.closest('.result-card');
                const notesTextarea = resultCard.querySelector('.radiologist-notes');
                const radiologistNotes = notesTextarea.value.trim();
                const imageName = resultCard.dataset.imageName;

                // Get the details from the existing card
                const severityRating = parseFloat(resultCard.querySelector('p:nth-child(3)').textContent.split(':')[1].trim());
                const comment = resultCard.querySelector('.truncate-text').dataset.fullText;
                const imageData = resultCard.querySelector('.result-image').src.split(',')[1];

                fetch('/save-image-notes', {
                    method: 'POST',
                    headers: {
                        'Content-Type': 'application/json',
                    },
                    body: JSON.stringify({
                        image_name: imageName,
                        radiologist_notes: radiologistNotes,
                        severity_rating: severityRating,
                        comment: comment,
                        image_data: imageData
                    })
                })
                    .then(response => response.json())
                    .then(data => {
                        if (data.message) {
                            alert('Notes saved successfully');
                            
                            // Move to history or update UI
                            const historyResults = document.getElementById('historyResults');
                            historyResults.innerHTML += createResultCard(
                                {
                                    ...resultCard.dataset,
                                    radiologist_notes: radiologistNotes,
                                    image_name: imageName,
                                    severity_rating: severityRating,
                                    comment: comment,
                                    image_data: imageData
                                }, 
                                true
                            );
                            resultCard.remove();
                        } else {
                            alert('Failed to save notes');
                        }
                    })
                    .catch(error => {
                        console.error('Error:', error);
                        alert('Failed to save notes');
                    });
            }
        });

        // Fetch history function
        function fetchHistory() {
            fetch('/view-history')
                .then(response => response.json())
                .then(data => {
                    const historyResults = document.getElementById('historyResults');
                    historyResults.innerHTML = '';
                    data.forEach(result => {
                        historyResults.innerHTML += createResultCard(result, true);
                    });
                })
                .catch(error => {
                    console.error('Error fetching history:', error);
                    showStatusMessage('Failed to fetch history.', 'info', 'historyResults');
                });
        }
    </script>
</body>
</html>
