document.addEventListener("DOMContentLoaded", function () {
    // Default Active Section
    document.getElementById("about").classList.add("active");

    // Function to Show Sections
    window.showSection = function (sectionId) {
        document.querySelectorAll(".section").forEach(section => {
            section.classList.remove("active");
        });
        document.getElementById(sectionId).classList.add("active");
    };

    // Typing Effect for Name
    const nameElement = document.querySelector(".name");
    const nameText = "Parth Kitchloo";
    let index = 0;

    function typeText() {
        if (index < nameText.length) {
            nameElement.innerHTML += nameText.charAt(index);
            index++;
            setTimeout(typeText, 150);
        }
    }

    nameElement.innerHTML = "";
    setTimeout(typeText, 500);

    // Smooth Scroll for Sidebar Links
    document.querySelectorAll(".sidebar a").forEach(link => {
        link.addEventListener("click", function (e) {
            e.preventDefault();
            const sectionId = this.getAttribute("onclick").match(/'([^']+)'/)[1];
            showSection(sectionId);
            window.scrollTo({ top: 0, behavior: "smooth" });
        });
    });
});
