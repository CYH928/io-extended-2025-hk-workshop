![image](https://github.com/user-attachments/assets/feb86924-8adc-4ec0-b0a1-91f1296a11e0)# Google I/O Extended 2025 HK Workshop


## Get the event GCP credits

1. Open [Redeem Page](https://trygcp.dev/e/iox25-HKG-azx), and Sign in with your **Personal** Google account.\
  ![image](https://github.com/user-attachments/assets/957b5df3-cfc7-4325-9725-1d48430638df)
2. Click **Access Your Credits**.\
  ![image](https://github.com/user-attachments/assets/8dcc1d7a-c3f7-45a4-b680-35ea29bab9ea)
3. Enter your name, then click the **Accept and continue** button.\
   ![image](https://github.com/user-attachments/assets/01b8a564-4f97-40f9-98dd-e4ca5afd09d7)
4. Please check the [Billing Account](https://console.cloud.google.com/billing/credits)'s **Credits** *(USD$5.00)*

---

## Open a new GDP Project

1. Open [Google Cloud console](https://console.cloud.google.com/).
2. In the top left area, select a project. After, create a new project named `io-extend-2025-workshop`, and choose the recently added **Billing account**.
3. Please confirm to selected your recently created **project**, and keep the **Project ID**.
4. At the [Vertex AI Page](https://console.cloud.google.com/vertex-ai) to **enable** the *Vertex AI API* in that project.

---

## Set up your Firebase Studio account

1. Go to [Firebase Studio](https://firebase.studio/), and click **Try Firebase Studio**.
2. **Accepted** the T&C for Firebase. Then, click **Confirm**.

---

## Firebase Studio run the Gemini Robotics

1. Open [Firebase Studio](https://studio.firebase.google.com/).
2. Click **Import Repo**, paste to Repo URL `https://github.com/wongcyrus/gcp-vertexai-gemini-robotics` and named it. After, click the **Import**.
3. Run the command at the terminal [Ctrl + J]
   ```shell
   git submodule update --init --recursive 
   ```
4. Open a new terminal.
5. At the new terminal, change directory to `robot-adk-agent` and `make install`.
   ```shell
   cd ~/gcp-vertexai-gemini-robotics/robot-adk-agent/
   make install
   ```
6. Set the project ID. Remember to change the `<your-project-id>` to your **Project ID**.
   ```
   gcloud config set project <your-project-id>
   ```
7. Run a command to authorise the project from the pop-up windows.
   ```
   gcloud auth application-default login
   ```
   1. Do you want to continue (Y/n)?  `Y`
   2. Press [Ctrl + Click] the sign-in link.\
      ![image](https://github.com/user-attachments/assets/66f39cb3-7770-475b-bcdc-b6e328f1ec78)
   3. Choose to same as your project account, click **Continue**.\
      ![image](https://github.com/user-attachments/assets/31fe607e-7f6a-4b1b-aa97-20d597e7db0c)
   4. At the *Sign in to the gcloud CLI*, click **Copy** and paste the verification code to terminal
      ![image](https://github.com/user-attachments/assets/000fcfde-c207-4daf-a59b-10cc5a1dc69f)
8. Set the project quota. Remember to change the `<your-project-id>` to your **Project ID**.
   ```
   gcloud auth application-default set-quota-project <your-project-id>
   ```
9. Modify the `SESSION_KEY` to your email at the `~/gcp-vertexai-gemini-robotics/robot-adk-agent/app/config.py`. Save it.\
    ![image](https://github.com/user-attachments/assets/cb2e7210-730b-46b0-a617-dd0fa0355fee)
10. Open a new terminal again.
11. At the new terminal, go to `robot-adk-agent` and `make local-backend`.
   ```shell
   cd ~/gcp-vertexai-gemini-robotics/robot-adk-agent/
   make local-backend
   ```
12. Wait a moment, select a Google Cloud Project, and click **Confirm** to let it open.\
    ![image](https://github.com/user-attachments/assets/ba9822cd-0733-46d3-812d-852946b288fc)
13. Open a new terminal again.
14. Run `make ui` in a new terminal.
   ```shell
   cd ~/gcp-vertexai-gemini-robotics/robot-adk-agent/
   make ui
   ```
15. Click the `http://localhost:8501`\
    ![image](https://github.com/user-attachments/assets/8ce837d2-2838-4756-b24a-af3c817e07e1)
16. Turn back to the `make local-backend` terminal, click to open `http://0.0.0.0:8000`
    ![image](https://github.com/user-attachments/assets/8bbc3f85-b46c-446f-a44b-ac4a85d61a0e)
17. Copy this link, and change the format from `https://` to `wss://`. Then, paste to Server URL.
    ![image](https://github.com/user-attachments/assets/79d446cf-8661-41a3-bfcb-08f7db7a379e)
    ![image](https://github.com/user-attachments/assets/6c75a93d-dbcc-4b37-bd67-189dd9d2dd8c)

