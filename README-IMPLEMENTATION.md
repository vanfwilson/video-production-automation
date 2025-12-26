# Video Production Automation System - Implementation Guide

## Setup Instructions

### Prerequisites
- Docker and Docker Compose installed
- - n8n instance running
  - - API credentials for:
    -   - Google Drive API
        -   - YouTube Data API v3
            -   - Anthropic Claude API
             
                - ### Installation Steps
             
                - 1. **Clone the repository**
                  2.    ```bash
                           git clone https://github.com/vanfwilson/video-production-automation.git
                           cd video-production-automation
                           ```

                        2. **Set up environment variables**
                        3.    ```bash
                                 cp .env.example .env
                                 # Edit .env with your API keys
                                 ```

                              3. **Import n8n workflows**
                              4.    - Open n8n dashboard
                                    -    - Import `workflow-01-raw-processor.json`
                                         -    - Import `workflow-02-publisher.json`
                                              -    - Configure API credentials in n8n
                                               
                                                   - 4. **Configure API Keys**
                                                     5.    - YouTube Data API v3 key
                                                           -    - Google Drive API credentials
                                                                -    - Claude API key
                                                                 
                                                                     - ## Workflow Details
                                                                 
                                                                     - ### Workflow 1: Raw Video Processing
                                                                     - - Input: Raw video file
                                                                       - - Process: YouTube transcription and AI editing
                                                                         - - Output: Editing instructions and metadata
                                                                          
                                                                           - ### Workflow 2: Video Publishing
                                                                           - - Input: Finished video file
                                                                             - - Process: YouTube publishing with auto-generated multilingual titles and descriptions
                                                                               - - Output: Published video with video ID
                                                                                
                                                                                 - ## Monitoring and Logs
                                                                                
                                                                                 - View logs in n8n interface or check the logs directory:
                                                                                 - ```bash
                                                                                   tail -f logs/n8n.log
                                                                                   ```

                                                                                   ## Troubleshooting

                                                                                   For issues or questions, refer to the main README.md
