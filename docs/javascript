document.addEventListener('DOMContentLoaded', function() {
  const moodTracker = document.getElementById('moodTracker');
  const moodOptions = document.getElementById('moodOptions');
  const moodHistory = document.getElementById('moodHistory');
  const moodDate = document.getElementById('moodDate');

  // A function to record the mood
  window.recordMood = function(mood) {
    let date = moodDate.value;
    if (!date) {
      alert("Please select a date");
      return;
    }

    // Store the mood in localStorage for demonstration
    localStorage.setItem(date, mood);

    // Update the display
    updateMoodHistory();
  };

  // A function to update the mood history display
  function updateMoodHistory() {
    moodHistory.innerHTML = "<h3>Mood History</h3>";
    let sortedDates = Object.keys(localStorage).sort().reverse(); // Sort dates
    sortedDates.forEach(function(date) {
      let mood = localStorage.getItem(date);
      moodHistory.innerHTML += `<div class="mood-entry"><strong>${date}:</strong> ${mood}</div>`;
    });
  }

  // Load the mood history when the page is loaded
  updateMoodHistory();

  // Listen for changes in the date input
  moodDate.addEventListener('change', updateMoodHistory);
});
