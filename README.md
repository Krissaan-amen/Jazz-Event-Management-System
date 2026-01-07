# PROJET-BDD-JAZZ

![Python](https://img.shields.io/badge/Python-3.8%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white)

## Overview

A comprehensive database management project implementing a **Jazz Concert Management System** using SQLite. This project demonstrates advanced SQL querying techniques, database design principles, and integration with machine learning models for natural language to SQL translation.

## Project Workflow

The notebook follows a structured approach to database management:

### 1. Database Setup
- **Connection**: Establishes connection to SQLite database `jazz_projet.db`
- **Schema Loading**: Imports database schema from `DATA.sql`
- **Error Handling**: Implements robust error handling for SQL operations

### 2. Data Population
- **Multi-source Data Import**: Loads data from various text files:
  - Client information (`xJazz_clients_all.txt`)
  - Musical pieces (`xJazz_morceux_et_arr_all.txt`)  
  - Musicians (`xJazz_musiciens_all.txt`)
  - Organizers (`xJazz_organisateurs_all.txt`)
  - Venues (`xJazz_salles_all.txt`)
- **JSON Integration**: Processes concert data from `donnees_concerts.json`

### 3. Database Schema

| Table | Purpose | Key Relationships |
|-------|---------|------------------|
| **Concert** | Main concert events | Links to Musicians, Organizers |
| **Client** | Customer information | Connected to Reservations |
| **Reservation** | Ticket bookings | Links Clients to Concerts/Sessions |
| **Musicien** | Artist profiles | Authors, Participants, Arrangers |
| **Salle** | Venue details | Hosts Sessions |
| **Organisateur** | Event organizers | Manages Concerts |
| **Morceau** | Musical pieces | Program compositions |
| **Programme** | Concert repertoire | Links Pieces to Concerts |
| **Seance** | Concert sessions | Specific date/venue combinations |

## Advanced SQL Queries

The project showcases sophisticated SQL techniques through 10 complex queries:

1. **Concert Program Data** - Multi-table joins for complete concert information
2. **Top Customers Analysis** - Customer ranking by ticket purchases (3 different approaches)
3. **Universal Attendees** - Clients attending all concert sessions
4. **Organizer Statistics** - Session counts per organizer
5. **Non-Arranger Musicians** - Musicians who never arranged pieces
6. **Revenue Analysis** - Total sales per concert
7. **Universal Repertoire** - Pieces played at all concerts
8. **Musician-Client Overlap** - Identifying musicians who are also customers
9. **Session Revenue** - Detailed financial breakdown per session (3 methods)
10. **Top Organizer** - Highest earning organizer (20% commission model)

## Technical Features

### SQL Techniques Demonstrated
- **Complex Joins**: Natural joins, left joins, multi-table relationships
- **Subqueries**: Nested queries and correlated subqueries
- **Window Functions**: RANK(), COUNT() OVER(), SUM() OVER()
- **Common Table Expressions (CTEs)**: Advanced query structuring
- **Aggregation Functions**: GROUP BY, HAVING clauses
- **EXISTS/NOT EXISTS**: Set operations and membership testing

### Machine Learning Integration
- **Text-to-SQL Translation**: Integration with Hugging Face models
- **API Integration**: Automated SQL generation from natural language
- **Model Evaluation**: Testing multiple pre-trained models for SQL generation

## Getting Started

### Prerequisites
- Python 3.8+
- SQLite3
- Required Python packages (see notebook imports)

### Installation & Usage

```bash
# Clone the repository
git clone https://github.com/Krissaan-amen/PROJET-BDD-JAZZ.git
cd PROJET-BDD-JAZZ

# Launch Jupyter notebook
jupyter notebook Final_Bdd_Code.ipynb
```

### Database Files Required
- `DATA.sql` - Database schema
- `Jazz_data/` directory with data files
- `donnees_concerts.json` - Concert information

## Key Insights

The project reveals important patterns in jazz concert management:
- Customer behavior analysis through purchase patterns
- Revenue optimization strategies for organizers
- Musical repertoire analysis across different concerts
- Operational insights for venue and session management

## Future Enhancements

- **Real-time Analytics**: Dashboard for live concert metrics
- **Recommendation System**: ML-based concert suggestions
- **Advanced NLP**: Improved natural language to SQL translation
- **Data Visualization**: Interactive charts and graphs
- **API Development**: RESTful services for database access

## Contact

For questions about database implementation or SQL optimization techniques:

**Email**: [amen.krissaan@gmail.com](mailto:amen.krissaan@gmail.com)

## License

This project is for educational and research purposes. Please cite appropriately if used in academic work.

---

*This project demonstrates the intersection of traditional database management with modern machine learning techniques, showcasing practical skills in both domains.*