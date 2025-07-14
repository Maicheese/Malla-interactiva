// script.js

const cursos = [
  { id: 1, nombre: "Química General I", prerequisitos: [] },
  { id: 2, nombre: "Técnicas de Laboratorio Químico", prerequisitos: [] },
  { id: 3, nombre: "Introducción al Álgebra y Cálculo", prerequisitos: [] },
  { id: 4, nombre: "Química Transformadora", prerequisitos: [] },
  { id: 5, nombre: "Razonamiento y comunicación científica", prerequisitos: [] },
  { id: 6, nombre: "Inglés I", prerequisitos: [] },
  { id: 7, nombre: "Química General II", prerequisitos: [1] },
  { id: 8, nombre: "Laboratorio de Química General", prerequisitos: [1, 2] },
  { id: 9, nombre: "Física General", prerequisitos: [3] },
  { id: 10, nombre: "Cálculo Diferencial e Integral", prerequisitos: [3] },
  { id: 11, nombre: "Biología Celular", prerequisitos: [2] },
  { id: 12, nombre: "Curso de Formación General", prerequisitos: [] },
  { id: 13, nombre: "Inglés II", prerequisitos: [6] },
  { id: 14, nombre: "Química Orgánica I", prerequisitos: [7] },
  { id: 15, nombre: "Química Analítica", prerequisitos: [7, 8] },
  { id: 16, nombre: "Laboratorio de Química Orgánica", prerequisitos: [7, 8] },
  { id: 17, nombre: "Estadística y Análisis de Datos", prerequisitos: [10] },
  { id: 18, nombre: "Física Aplicada a la Bioquímica", prerequisitos: [9] },
  { id: 19, nombre: "Fisiología Celular", prerequisitos: [9, 11] },
  { id: 20, nombre: "Cultura Científica: Divulgación y Enseñanza", prerequisitos: [4, 5] },
  { id: 21, nombre: "Química Orgánica II", prerequisitos: [14] },
  { id: 22, nombre: "Laboratorio de Análisis Químico", prerequisitos: [8, 15, 17] },
  { id: 23, nombre: "Química Analítica II", prerequisitos: [15] },
  { id: 24, nombre: "Fisicoquímica I", prerequisitos: [9, 10, 14] },
  { id: 25, nombre: "Fisiología de Sistemas", prerequisitos: [19] },
  { id: 26, nombre: "Taller de Cultura Científica", prerequisitos: [20] },
  { id: 27, nombre: "Curso de Formación General", prerequisitos: [] },
  { id: 28, nombre: "Laboratorio de Análisis Instrumental", prerequisitos: [22, 23] },
  { id: 29, nombre: "Bioquímica General", prerequisitos: [21] },
  { id: 30, nombre: "Estructura y Función de Organelos Celulares", prerequisitos: [21, 25] },
  { id: 31, nombre: "Fisicoquímica para Ciencias Biológicas", prerequisitos: [18, 24] },
  { id: 32, nombre: "Inglés III", prerequisitos: [13] },
  { id: 33, nombre: "Estructura y Función de Proteínas", prerequisitos: [29, 31] },
  { id: 34, nombre: "Genética Molecular", prerequisitos: [29] },
  { id: 35, nombre: "Inmunología Celular y Molecular", prerequisitos: [30] },
  { id: 36, nombre: "Microbiología General", prerequisitos: [30] },
  { id: 37, nombre: "Inglés IV", prerequisitos: [32] },
  { id: 38, nombre: "Química Fisiológica y Patológica", prerequisitos: [33, 35] },
  { id: 39, nombre: "Genética Molecular de Eucariontes", prerequisitos: [34] },
  { id: 40, nombre: "Fisiología y Genética Microbiana", prerequisitos: [34, 36] },
  { id: 41, nombre: "Administración y Gestión", prerequisitos: [26] },
  { id: 42, nombre: "Unidad de Investigación en Bioquímica", prerequisitos: [28, 29] },
  { id: 43, nombre: "Bioquímica Clínica y Patológica", prerequisitos: [38] },
  { id: 44, nombre: "Fisiología y Bioquímica Vegetal", prerequisitos: [39] },
  { id: 45, nombre: "Bioética", prerequisitos: [38] },
  { id: 46, nombre: "Formulación y Evaluación de Proyectos Científicos", prerequisitos: [33] },
  { id: 47, nombre: "Bioinformática", prerequisitos: [33, 39] },
  { id: 48, nombre: "Práctica Profesional I", prerequisitos: [33, 34] },
  { id: 49, nombre: "Laboratorio de Bioquímica Clínica", prerequisitos: [41, 43] },
  { id: 50, nombre: "Tópicos de Farmacología", prerequisitos: [43, 45] },
  { id: 51, nombre: "Biotecnología", prerequisitos: [43, 45] },
  { id: 52, nombre: "Electivo Especializado", prerequisitos: [] },
  { id: 53, nombre: "Electivo Especializado", prerequisitos: [] },
  { id: 54, nombre: "Práctica Profesional II", prerequisitos: [43, 47, 48] },
  { id: 55, nombre: "Unidad de Investigación Avanzada en Bioquímica", prerequisitos: [42, 49, 51] },
  { id: 56, nombre: "Bioprocesos Industriales", prerequisitos: [41, 51] },
  { id: 57, nombre: "Electivo Especializado", prerequisitos: [] },
  { id: 58, nombre: "Electivo Especializado", prerequisitos: [] },
  { id: 59, nombre: "Proyecto de Memoria de Título", prerequisitos: [46, 49, 50, 51] },
  { id: 60, nombre: "Memoria de Título", prerequisitos: [59] }
];

const aprobados = new Set();

function renderMalla() {
  const container = document.getElementById("malla-container");
  container.innerHTML = "";

  cursos.forEach(curso => {
    const div = document.createElement("div");
    div.className = "curso";
    div.id = `curso-${curso.id}`;
    const bloqueado = curso.prerequisitos.some(pr => !aprobados.has(pr));

    if (aprobados.has(curso.id)) {
      div.classList.add("aprobado");
    } else if (bloqueado) {
      div.classList.add("bloqueado");
    }

    div.innerHTML = `<h3>${curso.nombre}</h3><p>ID: ${curso.id}</p>`;

    if (!bloqueado || aprobados.has(curso.id)) {
      div.addEventListener("click", () => toggleCurso(curso.id));
    }

    container.appendChild(div);
  });
}

function toggleCurso(id) {
  if (aprobados.has(id)) {
    aprobados.delete(id);
  } else {
    aprobados.add(id);
  }
  renderMalla();
}

renderMalla();
