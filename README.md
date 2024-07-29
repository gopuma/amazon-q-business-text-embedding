# amazon-q-business-text-embedding
1. 	아래 사이트로 이동하여 상단의 Sign In 버튼을 누릅니다.
    https://www.voyageai.com
    <img width="1684" alt="Vectorize your data to gear" src="https://github.com/user-attachments/assets/88a42bcd-313b-40e7-b4a0-4fd477d75d35">

2.	자신의 이메일(구글 gmail 혹은 다른 개인 이메일)을 이용하여 Sign Up을 합니다.
    <img width="1828" alt="Screenshot 2024-07-26 at 4 20 53 PM" src="https://github.com/user-attachments/assets/d3d65bfc-9fee-4ccd-8ec8-8c80aa8962f7">

3.	Gmail 이외의 메일일 경우 아래와 같이 자신의 메일주소와 암호를 입력합니다.
    <img width="1452" alt="Screenshot 2024-07-26 at 4 21 25 PM" src="https://github.com/user-attachments/assets/08dec7b9-1cb4-45a3-acef-39c1109b4453">

4.	자신의 메일함으로 이동하여 아래 “VERIFY YOUR ACCOUNT” 버튼을  클릭합니다.
    <img width="609" alt="Verify Your Account" src="https://github.com/user-attachments/assets/fc5727b8-0509-462d-87ca-d6833371f398">

5.	인증이 완료되었으면 다시 https://www.voyageai.com 로 가서 sign in 합니다.
6.	로그인 한 후에 “Create new API Key” 버튼을 클릭하여 API Key를 생성합니다.
    <img width="1955" alt="Screenshot 2024-07-26 at 4 23 25 PM" src="https://github.com/user-attachments/assets/0b67fa69-70d6-4f7a-8674-f66ee4d29a7f">

7.	API key의 이름을 입력하고 “Create API Key” 버튼을 누릅니다.
    <img width="1949" alt="Screenshot 2024-07-26 at 4 23 46 PM" src="https://github.com/user-attachments/assets/5d586d42-c4c7-43fb-acdd-381cb12e0874">

8. API Key를 메모장에 복사해 둡니다.
    <img width="1951" alt="Screenshot 2024-07-26 at 4 23 59 PM" src="https://github.com/user-attachments/assets/2127ad51-0b8f-44fd-96a6-1c469507f96a">

9. 맥의 경우 Terminal을 윈도우의 경우 Powershell을 실행하고 apiKey를 export한다.
￼<img width="1165" alt="Screenshot 2024-07-28 at 5 51 10 AM" src="https://github.com/user-attachments/assets/5f9fec28-004d-4806-9b71-ec63050641b2">

10. 아래 curl 명령어와 위에 입력한 api key를 이용하여 “King”의 Text Embedding을 진행한다.
curl https://api.voyageai.com/v1/embeddings   -H "Content-Type: application/json"   -H "Authorization: Bearer $apiKey"   -d '{
    "input": "King",
    "model": "voyage-2"
  }'
<img width="1791" alt="Screenshot 2024-07-28 at 5 56 54 AM" src="https://github.com/user-attachments/assets/14ccdc88-cfd4-4fd2-b518-934f8c76b791">

11. curl 명령어와 위에 입력한 api key를 이용하여 “Queen”의 Text Embedding을 진행한다.
<img width="1795" alt="Screenshot 2024-07-28 at 5 58 34 AM" src="https://github.com/user-attachments/assets/fc584420-146c-4292-aa49-39e867a24916">

12. Cosine similarity를 알려주는 https://newtum.com/calculators/maths/cosine-similarity-calculator 사이트로 이동하여 King, Queen의 embedding 값을 입력한다.
<img width="1225" alt="Screenshot 2024-07-29 at 9 07 43 AM" src="https://github.com/user-attachments/assets/4166f114-c08a-4b7b-8be5-63dbd4020cff">


13. King과 Queen의 cosine similarity 값은 95.21%로 매우 유사하다는 것을 알 수 있다.
