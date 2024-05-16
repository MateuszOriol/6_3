docker run --name my-postgres-container -e POSTGRES_PASSWORD=mysecretpassword -d postgres

docker build -t my-express-app .
docker run -p 3000:3000 --link my-postgres-container my-express-app

Wyświetlenie wszystkich danych w tabeli: GET http://localhost:3000/data
Wyświetlenie n-tego wiersza w tabeli: GET http://localhost:3000/data/:id
Obliczenie średniej z pola typu liczba całkowita: GET http://localhost:3000/average