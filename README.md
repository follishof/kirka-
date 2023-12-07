// ==UserScript==
// @name         Redirect Loop kirka.io
// @namespace    https://your-namespace.com
// @version      1.0
// @description  Redirects from https://kirka.io/ to https://kirka.io/quests/hourly periodically
// @author       Your Name
// @match        https://kirka.io/*
// @grant        none
// ==/UserScript==

(function() {
    'use strict';

    function redirectToHourly() {
        if (window.location.href === 'https://kirka.io/') {
            window.location.href = 'https://kirka.io/games/OCEANIA~Gtnw8DPR';
        }
    }

    // Check every 5 seconds (5000 milliseconds)
    setInterval(redirectToHourly, 1000);
})();
