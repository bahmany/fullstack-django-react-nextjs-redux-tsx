# ReactJS, TSX, NextJS, Redux, Axios and Django REST
when we are working as a fullstack developer 

when we are working as a full stack developer with the rules below:
- Django rest as backend
- react as backend

we should use these items:

- Django rest framework
- Dj_rest_auth for auth and easy logins
- jwt
- Reactjs
- Redux
- Nextjs

The only problem is sending and receiving with backend with authenticated requests and responses.
To solving this problem for one of my projects I use the following solution:
- Using corsheaders for handling between front and back
- For example : 
    - back : https://localhost:8000
    - front: https://localhost:3000
- setup corsheaders completely 
- in setting.py
    - CORS_ALLOW_ALL_ORIGINS = False
    - CORS_ALLOW_CREDENTIALS = True
    - CORS_ALLOWED_ORIGINS = [
        - "http://localhost:3000",
        - "http://127.0.0.1:3000",
        - "https://localhost:3000",
        - "https://127.0.0.1:3000",
        - ]
- And in frontend:
    - const makeConfig = {
        - withCredentials:true,
        - crossDomain:true,
        - headers: this._header,
        - }
- For authenticating views:
    - permission_classes = (IsAuthenticated,)
    - authentication_classes = (JWTCookieAuthentication,)


that’s all !!!



https://rahsoon.com