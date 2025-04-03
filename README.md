# D'Hondt Calculator

A simple, interactive web-based calculator for simulating parliamentary seat distribution using the D'Hondt method. This tool allows users to experiment with different vote percentages and see how they translate into parliamentary seats.

Live demo: [https://resilient-raindrop-5fc6a7.netlify.app/](https://resilient-raindrop-5fc6a7.netlify.app/)

## Features

- **Interactive Vote Adjustment**: Use sliders to dynamically adjust vote percentages for each party
- **Real-time Calculation**: See seat distribution updates instantly as you modify votes
- **Party Management**:
  - Fix party votes: Lock a party's percentage while adjusting others
  - Hide parties: Remove parties from the calculation to focus on specific scenarios
- **Visual Results**: Seats are displayed as colored circles for easy visualization
- **Configurable Total Seats**: Adjust the total number of seats to be distributed

## How to Use

1. **Open the Calculator**:

   - Simply open `index.html` in any modern web browser
   - No server or installation required

2. **Adjust Votes**:

   - Use the sliders to set vote percentages for each party
   - Total percentage is automatically maintained at 100%
   - When you move one slider, others adjust proportionally

3. **Party Controls**:

   - Click the checkbox next to a party name to "fix" its value
   - Click the "Hide" button to remove a party from calculations
   - Hidden parties' votes are redistributed among visible parties

4. **Configure Seats**:
   - Set the total number of seats to be distributed using the input field at the top
   - Default is 350 seats
   - Supports between 1 and 1000 seats

## Technical Details

- Pure HTML/JavaScript implementation
- No external dependencies
- Mobile-friendly responsive design
- Uses the D'Hondt method for seat allocation:
  1. Divides each party's votes by 1, 2, 3, etc.
  2. Assigns seats to the highest quotients
  3. Continues until all seats are distributed

## D'Hondt Method Example

For a simple example with 10 seats and three parties:

- Party A: 100,000 votes
- Party B: 80,000 votes
- Party C: 30,000 votes

The votes are divided by 1, 2, 3, etc., and the 10 highest numbers determine the seat allocation:

1. 100,000 (A)
2. 80,000 (B)
3. 50,000 (A÷2)
4. 40,000 (B÷2)
5. 33,333 (A÷3)
6. 30,000 (C)
7. 26,666 (B÷3)
8. 25,000 (A÷4)
9. 20,000 (B÷4)
10. 16,666 (A÷5)

Final distribution: Party A: 5 seats, Party B: 4 seats, Party C: 1 seat

## Browser Compatibility

Tested and working in:

- Chrome
- Firefox
- Edge
- Safari

## License

This project is open source and free to use.
