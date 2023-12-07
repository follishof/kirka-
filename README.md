// ==UserScript==
// @name         Kirka.io Redirect and Reload
// @namespace    https://yournamespace.com
// @version      1.0
// @description  Redirects to a specified URL and reloads every 30 seconds if on the target page
// @match        https://kirka.io/*
// @grant        none
// ==/UserScript==

(function() {
    'use strict';

    // Set the target URL here
    const targetURL = 'https://kirka.io/games/OCEANIA~jyjW0Hbd3';

    // Function to redirect to the target page
    function redirectToTarget() {
        window.location.href = targetURL;
    }

    // Check if the current URL is the target page
    if (window.location.href === 'https://kirka.io/') {
        redirectToTarget(); // Redirect to the target page
    } else if (window.location.href === targetURL) {
        // If already on the target page, reload every 30 seconds
        setInterval(function() {
            location.reload();
        }, 30000); // 30 seconds in milliseconds
    }
})();
