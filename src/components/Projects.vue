<template>
    <section class="projects-section">
        <ul class="projects-container">
            <li class="project-card">
                <div class="card-content">
                    <h3 class="project-title">
                        <a href="#" target="_blank">KONOHA HOTEL PAGE</a>
                    </h3>
                    <div class="project-description">
                        <p>A minimal, dark blue theme for VS Code, Sublime Text, Atom, iTerm, and more. Available on Visual Studio Marketplace, Package Control, Atom Package Manager, and npm.</p>
                    </div>
                </div>
            </li>
        </ul>
    </section>
</template>

<style scoped>
.projects-container {
    list-style: none;
    padding: 0;
}
.project-card {
    position: relative;
    display: grid;
    gap: 10px;
    grid-template-columns: repeat(12, 1fr);
    -webkit-box-align: center;
    align-items: center;
}
.project-card .caed-content {
    grid-column: 1 / 9;
}
.project-card:nth-of-type(2n+1) .card-content {
    grid-column: 5 / -1;
}
.project-title {
    font-size: 28px;
    font-weight: 600;
}
</style>