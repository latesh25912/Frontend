<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css">
  <title>Flight Search</title>
  <style>
    body {
      padding: 20px;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Flight Search</h1>
    <form id="flightSearchForm">
      <div class="form-group">
        <label for="departure">From:</label>
        <input type="text" class="form-control" id="departure" required>
      </div>
      <div class="form-group">
        <label for="destination">To:</label>
        <input type="text" class="form-control" id="destination" required>
      </div>
      <div class="form-group">
        <label for="carrierID">Carrier ID:</label>
        <input type="text" class="form-control" id="carrierID" required>
      </div>
      <button type="submit" class="btn btn-primary">Search</button>
    </form>
    <div id="flightResults" class="mt-4"></div>
  </div>

  <script src="https://code.jquery.com/jquery-3.5.1.slim.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.5.4/dist/umd/popper.min.js"></script>
  <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js"></script>
  <script>
    document.getElementById('flightSearchForm').addEventListener('submit', function(event) {
      event.preventDefault(); // Prevent form submission

      // Get form input values
      var departure = document.getElementById('departure').value;
      var destination = document.getElementById('destination').value;
      var carrierID = document.getElementById('carrierID').value;

      // Simulate flight search
      var flightResults = simulateFlightSearch(departure, destination, carrierID);

      // Display flight results
      displayFlightResults(flightResults);
    });

    function simulateFlightSearch(departure, destination, carrierID) {
      // This is a dummy function to simulate flight search results
      var flights = [
        { flightNumber: 'FL001', departure: 'New York', destination: 'London', carrier: 'ABC Airlines' },
        { flightNumber: 'FL002', departure: 'London', destination: 'Paris', carrier: 'XYZ Airlines' },
        { flightNumber: 'FL003', departure: 'Paris', destination: 'New York', carrier: 'ABC Airlines' }
      ];

      // Filter flights based on search criteria
      var filteredFlights = flights.filter(function(flight) {
        return flight.departure.toLowerCase() === departure.toLowerCase() &&
          flight.destination.toLowerCase() === destination.toLowerCase() &&
          flight.carrier.toLowerCase().includes(carrierID.toLowerCase());
      });

      return filteredFlights;
    }

    function displayFlightResults(flightResults) {
      var resultsDiv = document.getElementById('flightResults');
      resultsDiv.innerHTML = ''; // Clear previous results

      if (flightResults.length > 0)
