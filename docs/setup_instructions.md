# FabRAG_1 Setup Instructions

This guide will help you set up and use the FabRAG_1 system, which is based on the GPT4All desktop application. FabRAG_1 allows you to run large language models (LLMs) locally and privately on your device, with a focus on Fab Academy content.

## System Requirements

- Operating System: Mac, Windows, or Linux
- Hardware: Any modern computer (GPU recommended for faster performance)

## Installing gpt4all

1. Download the GPT4All desktop application for your operating system:
   - [Download for Windows](https://gpt4all.io/installers/gpt4all-installer-win64.exe)
   - [Download for Mac](https://gpt4all.io/installers/gpt4all-installer-darwin.dmg)
   - [Download for Linux](https://gpt4all.io/installers/gpt4all-installer-linux.run)

2. Install and open the application. Additional information about this step can be found at [gpt4all's docs](https://docs.gpt4all.io/gpt4all_desktop/quickstart.html).

## Cloning the FabRAG_1 Repository

To obtain the necessary data and setup instructions for FabRAG_1, clone this repository to your local machine. Move to the directory where you want to store the repository and run the following command:

```bash
git clone https://github.com/lahoramaker/fabrag_1.git
```

Annotate the route of the repository in your local machine, as you will need to access the data for setting up the LocalDocs option later.

## Setting Up the Model

1. In the GPT4All application, click on "Models" in the left menu.
2. Click "+ Add Model" to navigate to the "Explore Models" page.
3. Search for and download the preferred text generation model: `llama-3.1-8B-instruct-128k`.
   
   **Note**: If you are part of an organization with more than 700 million monthly active users, you need a license to use the Llama 3.1 model. In this case, please choose an alternative model.

4. For embeddings, search for and download the "Nomic Embed v1.5" model. You need this embeddings model before processing LocalDocs.

## Setting Up LocalDocs

1. Click on "LocalDocs" in the left menu.
2. Click "+ Add Collection".
3. Name your collection (e.g., "FabAcademy_Docs").
4. Link it to one of the following folders:
   - webcontents-jina
   - webcontents-raw
   - webcontents-readability

   All of these folders contain plain text. Feel free to experiment with different folders and provide feedback on which works better.

5. Click "Create Collection". The embedding process will start. (If the process is too slow, don't forget to check the following note).

**Note on GPU Acceleration**: By default, GPT4All uses CPU to produce embeddings, which can be time-consuming. To accelerate the process:

1. Go to the LocalDocs settings.
2. Look for an option to use GPU for embeddings.
3. Enable this option
4. Restart gpt4all
5. Open LocalDocs to see how GPU significantly speeds up the embedding process. (Usually it takes less than one minute to process the whole collection).

## Using FabRAG_1

1. Go to "Chats" in the left menu.
2. Click "Load Default Model" (this should be the Llama 3.1 model you downloaded).
3. For new chats, click on the LocalDocs icon in the top-right corner.
4. Select your FabAcademy_Docs collection to include references from the most relevant Fab Academy papers.
5. Start chatting! The model will now use the Fab Academy content to inform its responses.
6. Citations to the original documents will appear below the generated text.

## Feedback

We welcome your feedback on which of the three LocalDocs folders (webcontents-jina, webcontents-raw, webcontents-readability) works best for your needs. Please share your experiences and suggestions for improvement.

## Troubleshooting

- If you encounter slow performance, ensure you have enabled GPU acceleration for embeddings in the LocalDocs settings.
- If you're unable to use the Llama 3.1 model due to licensing restrictions, try other available models in the GPT4All application.

For any other issues or questions, please refer to the GPT4All documentation or open an issue in the FabRAG_1 repository.
