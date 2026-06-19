function searchNotes() {

    let input =
        document.getElementById("searchBox")
        .value
        .toLowerCase();

    let notes =
        document.getElementsByClassName("note");

    for (let i = 0; i < notes.length; i++) {

        let subject =
            notes[i]
            .getElementsByTagName("h3")[0]
            .innerText
            .toLowerCase();

        if (subject.includes(input)) {

            notes[i].style.display = "block";

        } else {

            notes[i].style.display = "none";

        }
    }
}
