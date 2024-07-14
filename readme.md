# Lida Data Summarization and Visualization Demo

## Overview

This application demonstrates the use of the Lida Manager and OpenAI's GPT-3.5-turbo model for summarizing data and generating visualizations based on user queries. The application uses Streamlit for the web interface and integrates with OpenAI for text generation.

## Requirements

- Python 3.7+
- Streamlit
- OpenAI API
- dotenv
- Pillow (PIL)
- lida (Make sure you have the `lida` library installed, which may not be a standard library and could require specific installation instructions)

## Installation

1. Clone the repository:

    ```sh
    git clone https://github.com/aswin-bs/LIDA_DEMO_APP.git
    
    ```

2. Install the required dependencies:

    ```sh
    pip install streamlit openai python-dotenv pillow
    ```

3. Set up your environment variables. Create a `.env` file in the root directory and add your OpenAI API key:

    ```env
    OPENAI_API_KEY=your_openai_api_key
    ```

## Usage

1. Ensure you have the necessary API key set in your `.env` file.

2. Run the Streamlit application:

    ```sh
    streamlit run app.py
    ```

3. Use the sidebar to select between two options: "Summarize" or "Question based Graph".

### Summarize

1. Upload a CSV file using the file uploader.
2. The application will summarize the data and display the summary.
3. It will also generate goals based on the summary and visualize the first goal using a chart.

### Question based Graph

1. Upload a CSV file using the file uploader.
2. Enter a query in the text area to generate a graph based on your query.
3. Click "Generate Graph" to visualize the chart based on your query.

## How It Works

1. **File Upload**: Users can upload CSV files. The application saves these files locally.

2. **Data Summarization**: The Lida Manager uses OpenAI's GPT-3.5-turbo model to summarize the data. The summary method and text generation configuration are specified.

3. **Goal Generation**: Based on the summary, the application generates goals which are further used to create visualizations.

4. **Visualization**: The application generates charts using the specified goals or user queries. The charts are encoded in base64 format, decoded, and displayed using PIL and Streamlit.

## File Structure

- `app.py`: Main application file
- `.env`: Environment variable file containing API keys
- `requirements.txt`: List of required dependencies

## Additional Information

- **Text Generation**: The OpenAI API with GPT-3.5-turbo model is used for text generation tasks such as summarization and goal generation.
- **Visualization**: The charts are generated based on the summarized data and goals or user queries, and are displayed using Streamlit.

## Credits

This application uses the following libraries and services:
- [Streamlit](https://streamlit.io/)
- [OpenAI](https://www.openai.com/)
- [Pillow](https://pypi.org/project/Pillow/)

Feel free to contribute or raise issues if you find any bugs or have suggestions for improvements.