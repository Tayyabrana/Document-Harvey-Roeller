# Project Setup Instructions

## Clone the Rails API

1. **Clone the repository**:

    ```bash
    git clone https://github.com/Tayyabrana/Harvey-Roeller-Rails-API
    ```

2. **Navigate to the project directory**:

    ```bash
    cd Harvey-Roeller-Rails-API
    ```

3. **Install the required gems**:

    ```bash
    bundle install
    ```

4. **Set up the database**:

    ```bash
    rails db:create db:migrate db:seed
    ```

5. **Start the Rails server**:

    ```bash
    rails server
    ```

    The server will run at `http://localhost:3000` by default.

## Clone the React Native Mobile App

1. **Clone the repository**:

    ```bash
    git clone https://github.com/Tayyabrana/Harvey-Roeller-RN
    ```

2. **Navigate to the project directory**:

    ```bash
    cd Harvey-Roeller-RN
    ```

3. **Install the dependencies**:

    ```bash
    npm install
    ```

    or if you're using Yarn:

    ```bash
    yarn install
    ```

4. **Set up the base URL for the Rails API**:

    Open the file where `axiosInstance` is defined (usually in a folder like `src/api` or `utils`) and set the `baseURL` to the Rails API server address.

    ```javascript
    const axiosInstance = axios.create({
        baseURL: "http://192.168.1.12:3000/api/v1",
        headers: {
            'Content-Type': 'application/json',
        },
    });
    ```

    - Replace `http://192.168.1.12:3000` with your actual local IP address and Rails server port.

5. **Run the React Native app**:

    - For iOS:

    ```bash
    npx react-native run-ios
    ```

    - For Android:

    ```bash
    npx react-native run-android
    ```

    Ensure that your mobile device or emulator is connected and configured properly.

## Clone the React App

1. **Clone the repository**:

    ```bash
    git clone https://github.com/Tayyabrana/Harvey-Roeller-Web
    ```

2. **Navigate to the project directory**:

    ```bash
    cd Harvey-Roeller-Web
    ```

3. **Install the dependencies**:

    ```bash
    npm install
    ```

    or if you're using Yarn:

    ```bash
    yarn install
    ```

4. **Set up the base URL for the Rails API**:

    Open the file where `axiosInstance` is defined (usually in a folder like `src/api` or `utils`) and set the `baseURL` to the Rails API server address.

    ```javascript
    const axiosInstance = axios.create({
        baseURL: "http://192.168.1.12:3000/api/v1",
        headers: {
            'Content-Type': 'application/json',
        },
    });
    ```

    - Replace `http://192.168.1.12:3000` with your actual local IP address and Rails server port.

5. **Run the React app**:

    ```bash
    npm start
    ```

    or if you're using Yarn:

    ```bash
    yarn start
    ```

    The app will typically open in your default web browser at `http://localhost:3000`.

## Additional Notes

- Make sure your Rails API server is running and accessible from your React Native and React apps.
- Update the `baseURL` in both the React Native and React applications to match the IP address of the machine running the Rails server.
- If you encounter any CORS issues, make sure CORS is configured correctly in your Rails API.
