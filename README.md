# Cradle

## Firestore Database Structure

**Firestore Database Structure**

1. **Collection**: `communities`

   Each document in this collection has the following fields:

   - `name`: String - The name of the community
   - `owner`: String - The document id of the community owner in the `users` collection
   - `slug`: String - The unique identifier for the community

   **Document Examples**:

   - Document ID: `hhvlSXF6IIZcgnGUAnAj`

     - `name`: "Death Bats"
     - `owner`: "T5NZA326foNM0SO4oo9ZrxCf3Sb2"
     - `slug`: "dbc"

   - Document ID: `nKjCPAnIEak1FZunCEtl`

     - `name`: "Bored Apes"
     - `owner`: "sKrk4igurtR7B2q2SUGvHPExoMm2"
     - `slug`: "bayc"

   - Document ID: `vLhiL9neYdNQ3OLFWYCt`
     - `name`: "Wicked Craniums"
     - `owner`: "sKrk4igurtR7B2q2SUGvHPExoMm2"
     - `slug`: "wicked-craniums"

2. **Collection**: `users`

   Each document in this collection has the following fields:

   - `email`: String - The email address of the user
   - `fullname`: String - The full name of the user
   - `username`: String - The username of the user
   - `communities`: Array of String - The array of document ids from the `communities` collection indicating the communities that the user is part of

   **Document Examples**:

   - Document ID: `T5NZA326foNM0SO4oo9ZrxCf3Sb2`

     - `email`: "atharva@wisecounsel.ai"
     - `fullname`: "Wise Counsel"
     - `username`: "Wise Counsel"
     - `communities`: ["vLhiL9neYdNQ3OLFWYCt"]

   - Document ID: `sKrk4igurtR7B2q2SUGvHPExoMm2`
     - `email`: "atharva@wisecounsel.ai"
     - `fullname`: "Wise Counsel"
     - `username`: "Wise Counsel"
     - `communities`: ["hhvlSXF6IIZcgnGUAnAj", "nKjCPAnIEak1FZunCEtl", "vLhiL9neYdNQ3OLFWYCt"]

---

## Future Refinements:

- Change from Firebase compat to modular library
- Add Firebase analytics
